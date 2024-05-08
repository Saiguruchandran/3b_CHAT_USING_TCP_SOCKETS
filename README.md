# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME: SAIGURUCHANDRAN
### REG NO: 212223240143
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```

import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUTPUT
### CLIENT
![WhatsApp Image 2024-05-06 at 14 23 26_21cb8436](https://github.com/Saiguruchandran/3b_CHAT_USING_TCP_SOCKETS/assets/144870946/e70d7169-42a3-4cc2-902b-d1198237dbd8)

### SERVER
![WhatsApp Image 2024-05-06 at 14 23 42_2eb3f7c8](https://github.com/Saiguruchandran/3b_CHAT_USING_TCP_SOCKETS/assets/144870946/fb817644-9b50-497d-82e3-774dc76e4761)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
