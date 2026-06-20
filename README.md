# RFS (Remote File Server)
An RFS program that demonstrates the use of TCP (Transmission Control Protocol) message transfer as a continuous stream of bytes between its Client and Server hosts using TCP sockets. The program is defined by the commands:
- WRITE > Client transfers a file to the Server as bytes.
- GET > Client requests a file from the Server; if filename is valid and found then Server transfers to requesting Client.
- RM > Client requests to remove a file from the Server if filename is valid and file is found.
- STOP > Terminates the RFS program.

**Tech Stack: C, TCP/IP, Linux, VirtualBox, Makefile**

### Key Features
- TCP socket communication between client and server
- File transfer, retrieval, and deletion over a network
- Graceful program termination
- OOP design principles in C
- Systematic debugging with Valgrind

### Prerequisites
To be able to run the pipeline, make sure that the following prerequisites are complete:
1. C compiler
  - [Setting Up C Development Environment](https://www.geeksforgeeks.org/c/setting-up-c-development-environment/)
2. Set up 2 machines both with a Linux OS environment (1. Client / 2. Server):
  - Machines can be set up as a virtualization software such as VM VirtualBox on physical hardward or hosted on the cloud (Google, AWS, Azure, Oracle)

## Instructions
1. Clone the repository:  
`git clone https://github.com/lkim016/CS5600-PracticumII.git`
2. Access a first Linux environment (bash, wsl, etc.) for client.
3. Access a second Linux environment (bash, wsl, etc.) for Server.
3. Navigate / cd to exported files / folders with the Makefile.
4. Go to "src/config.h" to manually configure the required server IP Address, and/or other relevant configurations to set up the Client/Server under TCP (Transmission Control Protocol).
5. Run commands below inside the directory of the Makefile per first terminal and second terminal for Client/Server to execute based on the desired make commands:
  - `make server` - will compile the server program which will set it up to be ready to listen for connections and handle the client connection and its requests per the allowed commands.
  - `make client` - will compile the server program to be a client program which will set it up to be ready to send requests per the allowed commands to the server for the server to handle.
  <!-- - To exit the program, press [CTRL+C]. -->
