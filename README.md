### EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

DATE: 15-03-2023

AIM :
To write a python program to perform stop and wait protocol

### ALGORITHM :
# 1.Start the program.
# 2.Get the frame size from the user
# 3.To create the frame based on the user request.
# 4.To send frames to server from the client side.
# 5.If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.
# 6.Stop the program

PROGRAM :
CLIENT:
```
Developed by : SAKTHI PRIYA D
Register Number : 212222040139
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send(i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack)
        continue
    else:
        c.close()
        break
```
SERVER:
```
Developed by : SAKTHI PRIYA D
Register Number : 212222040139
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Received".encode())
```

OUTPUT :
CLIENT:
![image](https://github.com/sakthipriyadhanusu/EX-2/assets/119393194/7eb0c875-f429-4eb7-976c-922d0e6b0803)

SERVER:
![image](https://github.com/sakthipriyadhanusu/EX-2/assets/119393194/11a0adf2-9cf0-4d7d-b0b3-40fb56921dbd)

RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.



