# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client.py:
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
## Serevr.py:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
msg=input("Client > ") 
s.send(msg.encode()) 
print("Server > ",s.recv(1024).decode())
```
## OUTPUT
## Client.py:
<img width="482" height="262" alt="image" src="https://github.com/user-attachments/assets/67c1d082-a46b-4a5c-86e8-c3479f25ab7e" />

<img width="578" height="190" alt="Screenshot 2026-05-21 193016" src="https://github.com/user-attachments/assets/43c9d65d-2e51-47af-9d8d-cc74bb78fd47" />

## Server.py:
<img width="587" height="237" alt="Screenshot 2026-05-21 193108" src="https://github.com/user-attachments/assets/5cebc04a-c74d-418a-8b3a-fc45e6575fe9" />

<img width="553" height="185" alt="Screenshot 2026-05-21 193136" src="https://github.com/user-attachments/assets/ca2f54d2-1dcc-4902-8b3f-9a557e0e8b66" />

## Developed By: BUSHRA FATHIMA I
## Register Number: 212225040051

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
