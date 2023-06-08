# What is IIS?
IIS stands for Internet Information services and is a Microsoft .Net platform.

It can run on Windows, Linux and Mac OS.

As a web server, it's the processor behind hosting web applications.<br>
When hosting web application it becomes responsible for processing the applicaion messages
from default TCP ports. THe default port for HTTPS traffic, while 80 is the default port for HTTP traffic.
The traffic going into the IIS web server is sometimes reffered to as a web request.<br>
By default the traffic will come in through ports 443 and 80. This inbound traffic can be processed by the IIS web server in a few ways.

# How IIS Processes Requests
Typicly there are two main processing models.<br>
### Single-thread
### Thread-Per-Request
Thread-per-request is the default mode used by IIS.<br>
When a new request comes in a new thread is created speficly for that request.

The request is made through the HTTP protocol. The client sends a request and recieves a response.

# Modes
The IIS uses ts own process engine and a processing architecture, there are two layers, or modes
### Kernel Mode
When kernel mode is in use, code can execute any command and has total access to connected equipment. 
This mode is primarily used when a process is trusted and mostly invulnerable. Any crashes within kernel mode can do a lot of damage to the system itself. Kernel mode is also where you’ll find HTTP.SYS.
### User Mode
User mode is more limited. With this mode, executed code cannot access hardware or reference memory, giving you a more secure environment to work within. 
If a mistake is made, the consequences are unlikely to be as devastating as if the error had occurred in kernel mode. 
Executed code in user mode commands APIs to communicate with equipment and reference memory, which is much more secure than kernel mode. You’ll find the IIS Admin Service, application pools, and virtual directories in user mode.
