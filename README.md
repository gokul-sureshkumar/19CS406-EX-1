# 19CS406-EX-1 STUDY OF SOCKET PROGRAMMING WITH CLIENT-SERVER MODEL

DATE :

AIM :
```
To write a python program to perform stop and wait protocol

```

ALGORITHM :
```
1 Start the program. 
2. Get the frame size from the user 
3. To create the frame based on the user request. 
4. To send frames to server from the client side. 
5. If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client. 
6. Stop the program
```

```
## Server Program:
``` python 
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
	print(s.recv(1024).decode())
	s.send("Recieved".encode())
```

PROGRAM :
## Client Program:
## Developed by : GOKUL S
## Reg No: 212222110011
``` python
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
   i=input("ENter a data:")
   c.send(i.encode())
   ack=c.recv(1024).decode()
   if ack:
   	print(ack)
   	continue
   else:
   	c.close()
   	break
```
## Server Program:
``` python 
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
	print(s.recv(1024).decode())
	s.send("Recieved".encode())
```





OUTPUT:
## Server Output:
![image](https://github.com/gokul-sureshkumar/19CS406-EX-1/assets/121148715/ba6f0b14-dedf-4c7c-8d16-bf0fc207a727)
## Client Output:
![image](https://github.com/gokul-sureshkumar/19CS406-EX-1/assets/121148715/762bc1a6-362e-41c4-ad79-37459c13d937)




RESULT:
Thus, python program to perform stop and wait protocol was successfully executed.


