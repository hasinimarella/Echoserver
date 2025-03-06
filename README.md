# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

Name:MARELLA HASINI

REG NO:212223240083
```
server.py
import socket


HOST = "127.0.0.1"  
PORT = 65432  


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

client.py

import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hasini marella , 212223240083,06-03-2025")
    data = s.recv(1024)


print(f"Received {data!r}")




```
## OUTPUT:

![Screenshot 2025-03-06 113303](https://github.com/user-attachments/assets/196aa4b5-a919-44d0-ac55-e1a71432006f)


## RESULT:
The program is executed successfully
