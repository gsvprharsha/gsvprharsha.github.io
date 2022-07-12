---
title: Build a Port Scanner in just 41 lines using Python 3.0
tags: [Python 3.0, Linux, Ethical Hacking]
style: border
color: primary
description: A tutorial to build your very own Port Scanner using Python.
---
**Source:** [Github](https://github.com/gsvprharsha/port-scanner)

In this blog I will be showing, how you can create your very **own port scanner in just 41 lines of code**. This tutorial will be very simple and straight. I'll leave anything that I think is too complex. First, let's open an IDE for this. I am using **VS Code** in Kali Linux for this tutorial. Once you open your IDE; create a new file with any name, but make sure to put the extension as **.py**

Now, we are all set. Let's first import all the required modules that we would need for this tool. There are 3 modules in python which we are going to use.

```python
#!usr/bin/env python3 
import socket
from IPy import IP
from termcolor import colored
```

Now, we have imported all the required modules. Now, lets start with the first lines of code
```python
targets = input("[+]Enter the Target/s to initiate Scan(Split Multiple Targets with , ): ")
port_range = int(input("Enter the range of ports to scan(500 for first 500 ports): "))
if ',' in targets:
    for ip_add in targets.split(","):
        scan(ip_add.strip(" "), port_range)
else:
    scan(targets, port_range)
```

This part of the code takes 2 inputs from the user 
1. Targets 
2. Port Range

Next, we say need to differentiate multiple targets. For that, we have asked the user to use a  ```,```

So, now we use that principle and declare, that if  ```,```  in targets provided by the user; then for all the IP Addresses (declared here as ip_add), split for every value that comes after ```,```

And if we do not have ```,``` then send the input directly to the ```scan``` function. Now, let us write the ```scan``` function

```python
def scan(target, port_range):
    converted_ip = check_ip(target)
    print(colored("\n" + "[-_0]Scanning the target " + str(target), "yellow", attrs=['bold']))
    for port in range(1, port_range):
        scan_port(converted_ip, port)

def check_ip(ip):
    try:
        IP(ip)
        return(ip)
    except ValueError:
        return socket.gethostbyname(ip)
```

The scan function takes the two above mentioned parameters, and first check the ip using the ```check_ip``` function. This function checks if the given target input is an IP address or not. If it is an IP address; it will return back the address. But, if the target given is an ***URL***, then we use the ```socket``` module's inbuilt function; called ```.gethostbyname()``` to get the IP address of the URL and returns it to the ```converted_ip``` function. 

Once done, we print the statement that the scanning of the target is initiated. And For the port in range of 1 - ```port_range (given by user)```, we initiate a function called ```scan_port()``` function.

The ```scan_port()``` function is the function that will scan for the ports and return the result. So, let us write the ```scan_port()``` function

```python

def get_banner(s):
    return s.recv(1024)
    
def scan_port(ipaddress, port):
    try:
        sock = socket.socket()
        sock.settimeout(0.9)
        sock.connect((ipaddress, port))
        try:
           banner = get_banner(sock)
           print(colored("[+]Open Port " + str(port) + " " + str(banner.decode().strip("\n")), "green", attrs=['bold']))
        except:
            print(colored("[+]Open Port " + str(port), "green", attrs=['bold']))
    except:
        pass       # You can print a closed port statement here, but it confuses the user; so we pass without any print statement.
```

In this function we declare a variable ```sock``` which is equal to the ```socket()``` function that comes inbuilt with the socket module. Then, we set the timeout to 0.5 seconds. This is crucial because if we do not do this; the code will take a long time scanning each and every port. (You can set the timeout to a much higher value if you wish to)

And now, we connect to the IP address on that particular port. And then we try to get the banner of the response using the ```get_banner()``` function. And if we receive the banner we print that the port is open and we print the banner adjacent to it. And if we do not get any banner then, we just say the port is open. The ports in both these cases are open; this is so, because we received a response from the port. 

If we do not have an open port, then we say ```pass``` without printing any statement. Though you may print the statement that the port is closed. But it may confuse the user, so we have written pass in this case.

That's it, we completed the port scanner:smile:!!!

This is a very basic port scanner and it can be improved if you wish to.

Thanks for reading it this far :handshake:

Tomorrow I will be posting a blog on how to create your very own **Port Scan Detector**

# Resources
<a href="https://docs.python.org/3/library/socket.html">Socket Module</a><br>
<a href="https://pypi.org/project/IPy/">IPy Module</a><br>
<a href="https://pypi.org/project/termcolor/">Termcolor Module</a><br>
