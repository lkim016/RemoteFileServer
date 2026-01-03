# Practicum II - RFS (Remote File System)
A RFS program that demonstrates the use of TCP (Transmission Control Protocol) message transer as a continuous stream of bytes between its Client and Server hosts using TCP sockets. The program is defined by the commands:
- WRITE > Client transfers a file to the Server as bytes.
- GET > Client requests a file from the Server; if filename is valid and found then Server transfers to requesting Client.
- RM > Client requests to remove a file from the Server if filename is valid and file is found.
- STOP > Terminates the RFS program.

### Prerequisites
To be able to run the pipeline, make sure that the following prerequisites are installed:
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
  - `make client` - will compile the server program to be a `./rfs` program which will set it up to be ready to send requests per the allowed commands to the server for the server to handle.
  <!-- - To exit the program, press [CTRL+C]. -->

### References
[^1] [^2] [^3] [^4] [^5] [^6] [^7] [^8] [^9] [^10]

[^1]: "TCP/IP Protocol Design: Message Framing." codeproject, 20 Jun 2009. https://www.codeproject.com/articles/TCP-IP-Protocol-Design-Message-Framing#comments-section. Accessed: 2025-11-29.  
[^2]: "fseek() in C." GeeksforGeeks, 02 Aug 2025. https://www.geeksforgeeks.org/cpp/fseek-in-c-with-example/. Accessed: 2025-11-29.  
[^3]: "Socket Programming using TCP in C." SoftPrayog, 03 Oct 2018. https://www.softprayog.in/programming/network-socket-programming-using-tcp-in-c. Accessed: 2025-11-30.  
[^4]: "Socket Programming in C." GeeksforGeeks, 07 Aug 2025. https://www.geeksforgeeks.org/c/socket-programming-cc/. Accessed: 2025-12-01.  
[^5]: "Handling multiple clients on server with multithreading using Socket Programming in C/C++." GeeksforGeeks, 23 Jul 2025. https://www.geeksforgeeks.org/cpp/. Accessed: 2025-12-02.  
[^6]: Tom Herbert. "Protocol Header Design 101." Medium, 12 Oct 2025. https://medium.com/@tom_84912/protocol-header-design-101-1fcdb66582ba. Accessed: 2025-12-05.  
[^7]: "Using packed structures for network transmission." StackOverflow, 09 Dec 2022. https://stackoverflow.com/questions/74744741/using-packed-structures-for-network-transmission#74745980. Accessed: 2025-12-05.  
[^8]: "Length-prefix framing for protocol buffers." Eli Bendersky's Website, 02 Aug 2011. https://eli.thegreenplace.net/2011/08/02/length-prefix-framing-for-protocol-buffers?utm_source=chatgpt.com. Accessed: 2025-12-06. 
[^9]: "Introduction to Serial Framing Formats." DojoFive, 17 Apr 2025. https://dojofive.com/blog/introduction-to-serial-framing-formats/?utm_source=chatgpt.com. Accessed: 2025-12-06. 
[^10]: "Network Protocol Structures : Numbering." Sridar Sri. https://blog.sridarsri.com/network-protocol-structures-numbering/?utm_source=chatgpt.com. Accessed: 2025-12-06. 
