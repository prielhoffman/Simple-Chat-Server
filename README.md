# Socket Programming
## Overview

This project focuses on socket programming in the context of computer networks. It covers the implementation of both TCP and UDP communication protocols, along with a simple chat server and client application. The project consists of several small programs designed to help understand and apply the fundamentals of socket programming using TCP and UDP, as well as to explore network programming concepts like multiple socket handling using `select()`.

## Project Structure

The project is divided into four main parts:

1. **TCP Socket Programming**: 
   - Implementing a TCP sender and receiver to exchange data over a TCP connection.
   - Programs:
     - `TCP_sender.c`: Sends multiple parts of a file over a TCP connection to a receiver.
     - `TCP_receiver.c`: Receives data from a TCP sender.
   - Key functions: `socket()`, `bind()`, `listen()`, `accept()`, `send()`, `recv()`, `close()`.

2. **UDP Socket Programming**:
   - Implementing a UDP sender and receiver to handle data transmission using UDP.
   - Programs:
     - `UDP_sender.c`: Sends a stream of UDP messages to a receiver.
     - `UDP_receiver.c`: Listens for incoming UDP messages and processes them.
   - Key functions: `socket()`, `bind()`, `sendto()`, `recvfrom()`, `close()`.

3. **Select Server Programming**:
   - Developing a server using the `select()` function to manage multiple sockets simultaneously.
   - Program:
     - `Select_server.c`: Listens on multiple UDP ports and processes data received from clients.
   - Key functions: `select()`, `FD_SET()`, `FD_ISSET()`, `FD_ZERO()`.

4. **Chat Server and Client**:
   - Implementing a simple chat server and client using TCP for handling multiple clients simultaneously.
   - Programs:
     - `chat_server.c`: Manages a list of active clients and broadcasts messages.
     - `chat_client.c`: Connects to the server, sends messages, and listens for incoming messages.
   - Key functions: `socket()`, `bind()`, `listen()`, `accept()`, `send()`, `recv()`, `select()`.

### Running the Programs
## TCP Sender and Receiver
1. Run the TCP sender:

```bash
./TCP_sender <sender_address> <port> <number_of_file_parts> <file_name>
```

2. Run the TCP receiver:
```bash
./TCP_receiver <sender_address> <port> <number_of_file_parts>
```

## UDP Sender and Receiver
1. Run the UDP receiver:

```bash
./UDP_receiver <ip_address> <port> <number_of_file_parts>
```

2. Run the UDP sender:
```bash
./UDP_sender <ip_address> <port> <number_of_file_parts> <file_name>
```

## Select Server

Run the select server:

```bash
./select_server <port_1> <port_2> … <port_n>
```

## Chat Server and Client
1. Run the chat server:

```bash
./chat_server <port> <max_clients>
```

2. Run the chat client:
```bash
./chat_client <ip_address> <port> <user_name> <message>
```
