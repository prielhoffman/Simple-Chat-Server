# Multi-Client Chat Server in C

A networking project written in **C** that demonstrates practical socket programming through **TCP**, **UDP**, **`select()`-based I/O multiplexing**, and a **multi-client chat server**.

This repository brings together several low-level networking components, with the main focus on building a concurrent chat server and strengthening understanding of core communication patterns in client-server systems.

## Tech Stack

- **Language:** C
- **Networking:** TCP, UDP
- **System APIs:** Berkeley sockets, `select()`
- **Concepts:** socket programming, client-server architecture, concurrent connections, I/O multiplexing

## What the Project Includes

The repository contains several networking modules that cover different communication models:

- **TCP sender / receiver**
- **UDP sender / receiver**
- **`select()`-based server for handling multiple sockets**
- **Multi-client chat server and client**

Together, these programs demonstrate how to build and manage low-level communication systems in C.

## Main Features

- TCP-based communication between sender and receiver
- UDP-based message transfer
- Multi-client chat server
- Broadcast-style messaging between connected clients
- `select()`-based handling of multiple sockets
- Practical examples of connection setup, data transfer, and concurrent socket management

## Project Structure

### 1. TCP Communication

Implements basic TCP sender and receiver programs for reliable data transfer over a connection-oriented protocol.

**Files:**
- `TCP_sender.c`
- `TCP_receiver.c`

**Concepts covered:**
- connection establishment
- reliable stream communication
- sending and receiving data over TCP

### 2. UDP Communication

Implements sender and receiver programs for datagram-based communication.

**Files:**
- `UDP_sender.c`
- `UDP_receiver.c`

**Concepts covered:**
- connectionless communication
- datagram transfer
- packet-based message exchange

### 3. `select()`-Based Server

Implements a server that monitors multiple sockets simultaneously using `select()`.

**File:**
- `Select_server.c`

**Concepts covered:**
- I/O multiplexing
- handling multiple input sources
- event-driven socket management

### 4. Multi-Client Chat Application

Implements a TCP-based chat server and client for communication between multiple users.

**Files:**
- `chat_server.c`
- `chat_client.c`

**Concepts covered:**
- accepting multiple clients
- managing active client connections
- sending and receiving chat messages
- broadcasting messages across clients

## What I Implemented

This project was built to move beyond basic single-socket examples and practice real networking patterns in C.

Key implementation areas included:

- building socket-based programs with both TCP and UDP
- handling client-server communication using low-level system calls
- implementing a multi-client chat server
- using `select()` to manage multiple sockets concurrently
- structuring communication flows for different transport protocols
- practicing connection handling, message transfer, and socket lifecycle management

## Why This Project Matters

This project demonstrates practical understanding of:

- low-level network programming in C
- TCP vs. UDP communication patterns
- concurrent connection handling
- multiplexing with `select()`
- building multi-client server applications
- using system calls to manage sockets directly

It shows hands-on work with systems-level programming rather than only high-level networking libraries.

## How to Run

### TCP Sender and Receiver

Run the TCP sender:

```bash
./TCP_sender <sender_address> <port> <number_of_file_parts> <file_name>
```

Run the TCP receiver:

```bash
./TCP_receiver <sender_address> <port> <number_of_file_parts>
```

### UDP Sender and Receiver

Run the UDP receiver:

```bash
./UDP_receiver <ip_address> <port> <number_of_file_parts>
```

Run the UDP sender:

```bash
./UDP_sender <ip_address> <port> <number_of_file_parts> <file_name>
```

### `select()` Server

Run the server:

```bash
./select_server <port_1> <port_2> ... <port_n>
```

### Chat Server and Client

Run the chat server:

```bash
./chat_server <port> <max_clients>
```

Run the chat client:

```bash
./chat_client <ip_address> <port> <user_name> <message>
```

## Core Concepts Practiced

- `socket()`
- `bind()`
- `listen()`
- `accept()`
- `connect()`
- `send()` / `recv()`
- `sendto()` / `recvfrom()`
- `select()`
- `FD_SET()` / `FD_ISSET()` / `FD_ZERO()`
- `close()`

## Key Takeaways

Through this project, I strengthened my understanding of:

- how transport protocols differ in practice
- how to manage multiple client connections
- how multiplexing works with `select()`
- how to design simple communication systems in C
- how to work directly with networking APIs at the systems level

## Future Improvements

Possible next steps for the project:

- improve error handling and logging
- support richer chat commands
- add private messaging
- improve message formatting and client usability
- refactor repeated socket logic into shared utilities
- add documentation diagrams for communication flow
