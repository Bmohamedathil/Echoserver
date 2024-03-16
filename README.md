# Echoserver
Echo server and client using python socket

## AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
## Echo Client.py
```py
import socket
HOST = "127.0.0.1"  # This is Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
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
```
## Echo Server.py
```py
import socket
HOST = "127.0.0.1"  # This is Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
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
```

## OUTPUT:
### Client
![313386374-0331473a-25f5-4f88-9c54-ecb2a1da76e2](https://github.com/Bmohamedathil/Echoserver/assets/119560261/96994fb2-493d-45f3-8985-6e47df6d7a57)


### Server
![313386367-281956db-10e2-4004-a08a-a9fba17f12c9](https://github.com/Bmohamedathil/Echoserver/assets/119560261/9de2790b-68f5-4393-8132-2ac9f832f1b6)



## RESULT:
Thus the program is executed successfully.
