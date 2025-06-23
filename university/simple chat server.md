#chat-server #projects #multithreading 
# sockets:
they are a way to speak to other programs using standard Unix file descriptors
sockets are basically just a file which allows communication between different computers 
the file is a netwrok connection between 2 computers in this case

## internet sockets:
multiple type of sockets:
1. stream sockets->sock_stream
2. datagram sockets->sock_dgram
3. raw sockets

stream sockets are a reliable two way connected communication stream 
they use tcp to make sure that the data arrives error free to the other computer 

datagram sockets are connectionless, the data might arrive or it might not arrive
if it arrives it will arrive correctly
they are using udp 

# ip address
## subnets:
they are a smaller network within a larger network that help improve efficiency
they allow direct communication between devices reducing unnecessary routing 
# structs:
socket descriptor are just a regular int 
## addrinfor:
this is used to prepare the socket address structure for subsequent use 
its also used in host name lookups and service name lookups

![[Pasted image 20250301165427.png]]

- getaddrinfor returns a pointer to a new linked list of these structures filled out with what you need
- ai_family is used to force it to use ipv4 or ipv6
- ai_next points to the next element 
- ai_addr is a pointer to a struct sockaddr 


# multithreding
to have multiple people use the chat server at the same time multithreading is required

## reader writer problem
we need to ensure that there is no corruption
multiple readers are able to read at the same time but when a write operation is happening we need to ensure that only one writer and no one else is able to access the data 

## semaphores
they are responsible for the queue of the processes 
they keep a counter of how many processes they should let through and how many processes are in the queue
if the counter is positive then they should let that many number of processes through
if it negative then they should wait until they receive an instruction and the counter goes positive 
if its 0 then they should wait till they receive an instruction on what they should do. At that moment they are not going to do anything 

there 
## mutex:
they are meant to be taken and released 
they are essentially the shared resource being shared across different threads and they are use  semaphores to check whether someone is allowed to take them or if they are supposed to do nothing at the time. 

the difference between mutex and semaphores is that mutex only allows one thread to use it at a time while semaphores 

# ui on python 
sort of got it working 
its a really basic window so far but I will update it soon to have more functionality

