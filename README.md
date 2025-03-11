# Multithreaded Web Server in Java

## Overview
This project is a **Multithreaded Web Server** implemented in Java. It is designed to handle multiple client requests concurrently using **Java threads**, improving efficiency and responsiveness. The server can process HTTP requests, serve static files, and demonstrate fundamental networking principles.

## Features
- **Multithreading Support**: Efficiently handles multiple client requests simultaneously.
- **HTTP Request Handling**: Processes basic HTTP methods (GET, POST, etc.).
- **Static File Serving**: Serves HTML, CSS, JavaScript, and image files.
- **Logging Mechanism**: Logs incoming requests for debugging and analytics.
- **Graceful Shutdown**: Ensures proper resource cleanup on exit.
- **Configurable Parameters**: Allows modification of port, root directory, and thread limits.

## Technologies Used
- **Java** (Concurrency, Networking, I/O Streams)
- **Sockets API** (Server-Client Communication)
- **Multithreading** (Thread Pooling for concurrent requests)
- **HTTP Protocol Handling**

## Installation and Usage
### Prerequisites
- Java 11 or later installed
- Basic knowledge of networking and HTTP

### Clone the Repository
```sh
$ git clone https://github.com/Girishkyal/Multi-threaded-Web-Server.git
$ cd MultithreadedWebServer
```

### Compile the Project
```sh
$ javac WebServer.java
```

### Run the Server
```sh
$ java WebServer <port_number> <root_directory>
```
**Example:**
```sh
$ java WebServer 8080 ./www
```
This starts the server on **port 8080**, serving files from the `www` directory.

## How It Works
1. The server starts and listens on a specified port.
2. When a client (browser) sends an HTTP request, a new thread is spawned to handle it.
3. The server reads the request, determines the requested file, and responds accordingly.
4. If the requested resource exists, it is sent back with the correct HTTP status; otherwise, a **404 Not Found** page is returned.
5. The server logs all requests and responses.

## Sample Output
```
Server started on port 8080
New client connected: 192.168.1.10
GET /index.html HTTP/1.1
Serving file: index.html
Client disconnected: 192.168.1.10
```

## Enhancements and Future Work
- Implement HTTPS support
- Add CGI support for dynamic content
- Support for HTTP 1.1 Keep-Alive connections
- Improve request parsing and error handling

## Contributing
Pull requests are welcome. If you'd like to contribute, please fork the repository and submit a PR with detailed descriptions of changes.


