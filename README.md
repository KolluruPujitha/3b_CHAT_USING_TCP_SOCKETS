# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME:K.PUJITHA

## REG NO:212223240074
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
## Client
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client>")
 s.send(msg.encode())
 print("Server>",s.recv(1024).decode())

## Server
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client>",ClientMessage)
 msg=input("Server>")
 c.send(msg.encode())

```
## OUTPUT
## CLIENT
![Screenshot 2024-10-19 114404](https://github.com/user-attachments/assets/9d519d7b-1c3d-4274-8069-e42838167bcb)
## SERVER
![Screenshot 2024-10-19 114439](https://github.com/user-attachments/assets/8d543521-4efe-4f2a-ad29-6db9d14cd9b7)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
