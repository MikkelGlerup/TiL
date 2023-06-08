# What is IIS?
IIS stands for Internet Information services and is a Microsoft .Net platform.

It can run on Windows, Linux and Mac OS.

It is primarily used for hosting .NET web applications, howver, it can also be used as an FTP server and for hosting WCF services. It can also
host on other platforms (like PHP) when extended.

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

Kernel mode is use to make use of HTTP.SYS, to accept incoming client requests.

# Why IIS Web Server
IIS is used because of their keys features:
### Application Pools
Application pools can have zero or many IIS worker processes running. These worker processes are responsbile for running application instances. <br>
Pools can have 2 modes: Classic or intergrated<br>
#### Intergrated
Integrated mode is more commonly used.<br>
If a pool is intergrated then ,NET is a part of the IIS request pipeline
#### Classic
If a pool is classic, then there's one pipeline for the IIS and a seperate one for the .NET.
### Authentication
IIS boasts authentication features such as: 
#### Windows auth
#### Basic
#### Windows ACtive Diretory
### Security
IIS comes with security features such as utilities for managing TLS certficates, binding so SFTP and HTTPS can be enabled.<br> The ability to whitelist and blacklist traffic
### Remote Management

# References
https://www.dnsstuff.com/windows-iis-server-tools [08/06/2023]
