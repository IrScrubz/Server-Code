# Server-Code
This is a simple code for my server socket.

import socket
s = socket.socket()
host = socket.gethostname()
port = 9999
s.bind((host, port))
print("Hi Scrubz, waiting for connection...")
s.listen(5)
while True:
    conn,addr = s.accept()
    print("Got connection from ", addr)
    conn.send(b'Server Saying Hi')
    conn.close()
