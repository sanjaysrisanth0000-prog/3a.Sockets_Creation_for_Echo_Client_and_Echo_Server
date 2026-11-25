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
server:
```
import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)

c, addr = s.accept()

while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
client:
```
import socket

s = socket.socket()

s.connect(('localhost', 8000))

while True:
    msg = input("Client > ")
    s.send(msg.encode())

    print("Server > ", s.recv(1024).decode())
```
## OUPUT
server:
<img width="1917" height="1078" alt="Screenshot 2026-11-25 091218" src="https://github.com/user-attachments/assets/64c709fb-2717-4a05-9c37-38cf33a4d607" />

client:
<img width="1917" height="1077" alt="Screenshot 2026-11-25 091205" src="https://github.com/user-attachments/assets/46ca348e-cb8d-4cb2-94e8-4970bc1c7b0a" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
