Experiment 7

Implementation of remote command execution using socket system calls.
Table of contents

    Description
    Initiation
        To build
        Start processes
        To clean executables
    Execution
        Successful connection
        Failed connection - Bad command given

Description

    Basic client-server model.
    Server executes commands sent by client.
    Client asks for command to be executed, which is sent to the server to execute.
    Concurrent server, multiple clients can be opened and serviced at the same time.

Initiation
To build

make all

Start processes

    Server

./remoteserver

    Client (on localhost)

./remoteclient 127.0.0.1
