# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

### AIM :

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

### ALGORITHM :

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server.
4. Send and receive the message using the send function in socket.

### PROGRAM :

### CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER :
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

### OUTPUT :

### CLIENT :

![image](https://github.com/Anandanaruvi/EX-8/assets/120443233/6b7e065a-195d-4406-9239-5486ce67436d)

### SERVER :

![image](https://github.com/Anandanaruvi/EX-8/assets/120443233/e4e57593-645e-440a-b3c5-d98d0b485831)

### RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
