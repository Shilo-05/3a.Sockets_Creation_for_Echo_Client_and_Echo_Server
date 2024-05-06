# 3(A).CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
### Name: Oswald Shilo
### Reg No: 212223040139

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
 c.send(ClientMessage.encode())
```
## OUPUT
![Screenshot 2024-04-29 134131](https://github.com/YASHWINISEC/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/139361633/e24d33fc-083c-461d-98e4-ffaafdd29d51)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
