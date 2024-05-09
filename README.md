# Ex No :3a  CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME : ARAVINDAN D
## REGISTER NUMBER : 212223240012
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
### CLIENT 
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())

```
### SERVER 
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT
### CLIENT OUTPUT
![Screenshot 2024-05-09 125816](https://github.com/Aravindan2006/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151760062/82c7254c-7f71-4150-a510-4c3fe9459ff7)

### SERVER OUTPUT
![Screenshot 2024-05-09 125825](https://github.com/Aravindan2006/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151760062/3fe54ead-7911-4e91-b72c-b462bb12df34)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
