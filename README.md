# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name: GURU REVANTH KUMARAVEL RADHIKA
## Register Number: 212223230065
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Server Side
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
### Client Side
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUTPUT
## CLIENT:
 ![Screenshot 2024-04-29 140608](https://github.com/23013743/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/161271714/ce5c36df-ba09-4ed1-9bbd-62906c376ac9)

## SERVER:
 ![Screenshot 2024-04-29 140615](https://github.com/23013743/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/161271714/538e0189-db9f-4167-973f-a7ddd3434b9d)
## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
