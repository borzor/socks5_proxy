<sub><sup>this project created for educational purposes</sup></sub>
#  SOCKS5 Server 
Socks5[(RFC)](https://tools.ietf.org/html/rfc1928) multithread asynchronous proxy server with using boost::asio callbacks

#### It supports address types:
* `IPv4`
* `DOMAINNAME`
* `IPv6`

#### Supported authentication methods 
* `NO AUTHENTICATION REQUIRED` 
* `Username/Password Authentication for SOCKS V5`[(RFC)](https://tools.ietf.org/html/rfc1929)

# SOCKS5 Client
Socks5 multithread client based on [Reactor](https://www.adamtornhill.com/Patterns%20in%20C%205,%20REACTOR.pdf) pattern with poll in Synchronous Event Demultiplexer.
Created for server load testing. 



## Build
Clone the repository
```
git clone https://github.com/borzor/socks5_proxy
```
### Linux
Download boost library and CMake and run the followings commands


Configure project with СMake
* For server
```
cd /socks5_proxy/server
cmake ./CMakeLists.txt 
cmake --build .
```
* For client
```
cd /socks5_proxy/client
cmake ./CMakeLists.txt 
cmake --build .
```
Run the program
```
./server [listen-port] [number_of_threads]
```
```
./client  [listen-port] [target-port] [number_of_threads] [buffer_size] [number_of_clients] [time_on_test]
```

