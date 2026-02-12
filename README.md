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
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())

```

## OUPUT
<img width="957" height="202" alt="Screenshot 2026-02-12 112146" src="https://github.com/user-attachments/assets/221d9b36-1734-4132-9e0a-f2066b40e872" />
<img width="1044" height="167" alt="Screenshot 2026-02-12 112123" src="https://github.com/user-attachments/assets/dbf86eb7-53c6-4fa5-b43d-c71e9c3b4a56" />


Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
