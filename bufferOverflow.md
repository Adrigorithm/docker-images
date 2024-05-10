docker run --name buffer_overflow buffer_overflow_demo
docker exec -it buffer_overflow
./hacked

-> show code
-> wrong password
-> trigger segfault

dmesg | tail

-> copy instruction address
-> bytes.fromhex("ADDRESS")

objdump -d ./hacked | less

-> copy <debug> address
COMPILE <debug>: 

Python file
```
import sys

# = debug address

payload = b""
payload += b""[::-1]

sys.stdout.buffer.write(payload)
```

-> figure out overflow
-> set payload before overflow
-> add bytes of debug address
-> pipe payload to program
-> keep file descriptors up (python3 payload.py; cat) | ./hacked
