Experiment 5

Write a program to implement concurrent chat server that allows a client to chat with the server.
Table of contents

    Description
    Initiation
        To build
        Start processes
        To clean executables
    Execution
        Successful communication
        Failed connection - Multiple clients
        Failed connection - Missing address

Description

    TCP iterative client-server model.
    Server is a chatserver, communicates independently with the client connected.
    Doesn't support multiple clients at the same time.
    Hence, clients cannot communicate with each other, as there can only be one client at a time.
    Client is prompted for input, to be sent to the server.
    Server recieves client input, displays it and sends a response back to the client.
    Client recieves server reply, and process continues.
