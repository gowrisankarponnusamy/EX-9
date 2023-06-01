# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

### DATE : 03-05-2023

### AIM :
To write a python program for creating Chat using TCP Sockets Links

### ALGORITHM :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module
in server
4. Send and receive the message using the send function in socket.

### PROGRAM :
### CLient:
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
print("Client > ",ClientMessage)
msg=input("Server > ")
c.send(msg.encode())
```

### OUTPUT :
### Client:
![image](https://github.com/gowrisankarponnusamy/EX-9/assets/119393123/cb43f6ae-e38c-4a46-ba25-ceb7a6dca4d8)
### Server:
![image](https://github.com/gowrisankarponnusamy/EX-9/assets/119393123/b28ffd48-9286-42d6-a547-b814d8761a12)
### RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
