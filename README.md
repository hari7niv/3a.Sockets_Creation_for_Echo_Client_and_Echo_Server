# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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
## Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    cm=c.recv(1024).decode()
    c.send(cm.encode())
```
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client : ")
    s.send(msg.encode())
    print("Server : ",s.recv(1024).decode())
```
## OUPUT
![image](https://github.com/user-attachments/assets/119a0816-7868-437f-985f-2e632cccfcab)

![image](https://github.com/user-attachments/assets/09e25564-b4bb-4b2a-8339-97bc81a84aa7)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
