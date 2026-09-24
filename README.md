# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## AIM:

To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.

## PROGRAM

### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT :

<img width="921" height="414" alt="image" src="https://github.com/user-attachments/assets/ee8f4a69-7306-4d8b-9e97-019585a12528" />

## SERVER :

<img width="628" height="58" alt="image" src="https://github.com/user-attachments/assets/66dfdb3b-4352-472d-88da-85959b1ebbd3" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
