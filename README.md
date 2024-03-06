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
## OUTPUT

## CLIENT
![3 2 1](https://github.com/shaikSameerbasha5404/3b_CHAT_USING_TCP_SOCKETS/assets/118707756/e4d0ed30-1ba6-49f9-8ba7-7479714b3386)

## SERVER
![3 2 2](https://github.com/shaikSameerbasha5404/3b_CHAT_USING_TCP_SOCKETS/assets/118707756/2314441a-f679-489f-96e5-42601363b5dd)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
