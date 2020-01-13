[![PyPI version](https://badge.fury.io/py/psocket.svg)](https://badge.fury.io/py/psocket)
[![Build Status](https://travis-ci.org/c-pher/PSocket.svg?branch=master)](https://travis-ci.org/c-pher/PSocket)
[![Coverage Status](https://coveralls.io/repos/github/c-pher/PSocket/badge.svg?branch=master)](https://coveralls.io/github/c-pher/PSocket?branch=master)


# PSocket
The cross-platform simple tool to work with remote server through sockets. 
It can establish socket connection to a remote host:port, send commands and receive response.
No need to send byte-string. Use usual strings to send command.

## Installation
For most users, the recommended method to install is via pip:
```cmd
pip install psocket
```

or from source:

```cmd
python setup.py install
```

## Import
```python
from psocket import SocketClient
```
---
## Usage
```python
from psocket import SocketClient

client = SocketClient(host='172.16.0.48', port=3261)
print(client.greeting())
```
```python
from psocket import SocketClient

client = SocketClient(host='172.16.0.48', port=3261)
print(client.send_command(b''))
```

---

## Changelog
##### 1.0.0a2 (13.01.2020)
Reverted "client". Now it is attribute again to keep session alive 

##### 1.0.0a1 (13.01.2020)
- Now connection creates with client property
- New methods added:
    - is_host_available() 
    - get_sock_name()
    - get_peer_name()

##### 1.0.0a0 (13.01.2020)
- initial commit
