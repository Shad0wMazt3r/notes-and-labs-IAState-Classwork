
# Application Level Security

### TCP Stream Service 
- Simple way for Aplication to send data
- App just has to write to TCP 
    - Will send if not write for a while or if told to send

![stream](./stream.png)

### Sockets
- Application to TCP interace
    - Asking OS to use TCP 
    - Get back handle (way file is described)

![app](./app_tcp.png)

- Socket Protocol

![protocol](./protocol.png)

### C Sockets Server
- Nsdaddr.sin 
    - Server
    - Family
    - s_addr
    - port =  htons(num)
- vs = socket(AF_NET, SOCK_STREAM, 0)
    - Can use other than sock stream for different things like UDP
- bind(vs, nsaddr, sizeof(nsaddr))
- listen(vs, 5)
    - How many connects to allow until drop
- ns = accept(vs, from_addr, from_len)

### Client 
- gethostbyname()

### Web 
- Get connecttion and fork

![web](./web.png)


### Vulnerabilities

- Have common attacks
- Limited to application
- Can allow access to the computer 
    - Privileged apps are target

### Header Based
- Common
- Have freeform header 
- Parsing data sent to it instead of fields like IP ...
- Buffer overflow is common

![buff](,/bufferoverflow.png)


### Protocol Based
- Application specific 
- Part of authentication attack

### Auth Based
- Most common
- Two types
- Direct
    - Using the application authentication mechanism to gain access \
    - Password spraying
- Indirect
    - Using one of the other attack categories to circumvent authentication


### Traffic Based
- DOS
- Sniffing




