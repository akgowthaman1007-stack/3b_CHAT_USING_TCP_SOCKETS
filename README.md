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
~~~
client.py

import socket
s=socket.socket()
s.connect(('localhost',9300))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
~~~
~~~
server.py

import socket
s=socket.socket()
s.bind(('localhost',9300))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
~~~
## OUPUT
client.py

<img width="1481" height="288" alt="564880597-1b99b52c-b9fb-48e6-b908-351e3e65f5f5" src="https://github.com/user-attachments/assets/e9fa9fc2-ba07-4ba5-98a1-6e28ac65545c" />


server.py

<img width="1483" height="284" alt="564880745-8ebd620d-c05b-4268-9fea-7881391b967d" src="https://github.com/user-attachments/assets/00fcb28f-b1e3-48e2-a87d-fd25436a094b" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
