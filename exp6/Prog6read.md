# Program 6 - Echo client/Server

## TOC
- [Program 6 - Echo client/Server](#program-6---echo-clientserver)
  - [TOC](#toc)
  - [Program Description](#program-description)
  - [Iterative](#iterative)
    - [Output](#output)
      - [Client incorrect address](#client-incorrect-address)
      - [Successful echos](#successful-echos)
  - [Concurrent](#concurrent)
    - [Output](#output-1)
      - [Client incorrect address](#client-incorrect-address-1)
      - [Successful communication](#successful-communication)

## Program Description

The communication process is this minimal orocess:

1. Client sends string size to server
2. Client sends string to server
3. Server sends string back to client

The iterative and concurrent versions share the same client (As it is a design of the server)

## Iterative

The server maintains one thread and responds with it. Multiple requests are queued for response, and dealt with in a FIFO manner.

### Output

#### Client incorrect address

Two cases are shown here:
1. Client cannot connect as server isn't running
2. Insufficient arguments provided

![Incorrect client](Screenshot%20from%202020-11-02%2015-31-05.png)


#### Successful echos

It can be seen that all the processes share the same pid, showing that the same process is being used

![Successful echoes](Screenshot%20from%202020-11-02%2015-28-47.png)

## Concurrent

The server forks to respond to the client. Additionally, a signal handler needs to be present, to remove the exit child processes after they have responded to the client.

### Output

#### Client incorrect address

Two cases are shown here:
1. Client cannot connect as server isn't running
2. Insufficient arguments provided

![Incorrect client](Screenshot%20from%202020-11-02%2015-31-05.png)

#### Successful communication

The different pids depict that the process forks in order to respond. This allows multiple clients to connect to the server and communicate with it at the same time.

![Concurrent successful](Screenshot%20from%202020-11-02%2015-37-36.png)