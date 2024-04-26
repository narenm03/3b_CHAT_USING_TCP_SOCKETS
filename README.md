# 3b.CREATION FOR CHAT USING TCP SOCKETS
## name:NARENDHARAN.M
## reg no: 212223230134
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server.py:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT
## client Window:
![image](https://github.com/narenm03/3b_CHAT_USING_TCP_SOCKETS/assets/152469427/e953ee77-7088-4509-899b-cb1397698c1a)

## server Window:
![image](https://github.com/narenm03/3b_CHAT_USING_TCP_SOCKETS/assets/152469427/e4a2185d-66a8-4254-871a-f95d036b5250)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
