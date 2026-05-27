# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

CLIENT:
```
#DEVELOPED BY: DHANAVISHNI M
#REGISTER NO: 212225040064
import socket 
s=socket.socket() 
s.bind(('localhost',12345)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
```
SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',12345)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT:
CLIENT:
<img width="1919" height="1018" alt="Screenshot 2026-05-27 130952" src="https://github.com/user-attachments/assets/b2cc52c8-17e4-4f93-9a29-2e70a1b75736" />
SERVER:
<img width="1919" height="1016" alt="Screenshot 2026-05-27 131012" src="https://github.com/user-attachments/assets/a90dfb8f-38b8-4d0b-a817-29273b0e1d79" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
