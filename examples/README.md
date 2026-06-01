    
### The examples work in pairs, a sender and a receiver. 

####  recvfile.py and sendfile.py 

* start sendfile.py
```py3
python3 sendfile.py


startup: ✓
ipv4int: ✓
create_socket: ✓
setsockflag: ✓
bind: ✓
listen: ✓
listening on srt://0.0.0.0:9000
Waiting for connections...

```
* run recvfile.py with srt_url, remote_file_name, local_file_name
* sendfile is bound to 0.0.0.0:9000 by default, so for __srt_url__  use __srt://127.0.0.1:9000__
* let's use __test-c-client.py as our remote_file_name__ and __tcc.py as the local_file_name__
```sh
python3 recvfile.py srt://127.0.0.1:9000 test-c-client.py tcc.py
startup: ✓
ipv4int: ✓
create_socket: ✓
setsockflag: ✓
connect: ✓
rfl b'\x10'
send: ✓
request_file: ✓
send: ✓
request_file: ✓
buffer.value  b'535'
remote file size 535
remote_file_size: ✓
remote size recv 535
recvfile: ✓
recvsize 535

```









   
