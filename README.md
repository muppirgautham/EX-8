## EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER:
```
DATE : 27-04-2023
```
## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the 
  Socket module in server.
4.Send and receive the message using the send function in socket.
```
## PROGRAM :
```
Developed by: M Gautham.
Register No: 212221230027
```

### Client_Side:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### Server_Side:
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
## OUTPUT :
### Client_Side:

![image](https://github.com/muppirgautham/EX-8/assets/94810884/e51edb2b-893a-406d-93ac-ea4562f34ec2)
### Server_Side:

![image](https://github.com/muppirgautham/EX-8/assets/94810884/6b1f789a-468c-4b72-8293-32f3e444224f)

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
