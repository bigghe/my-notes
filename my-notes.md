
# AWS

## Service

- TorchServe: AWS service for PyTorch (which is the most popular open source libraries for deep learning)

- AWS Transfer: SFTP, FTP and FTPS service managed by AWS.

- AWS SAM (Serverless Application Model): is an open-source framework that you can use to build serverless applications on AWS. AWS SAM let you test and debug serverless application locally too.

- AWS Keyspaces (for Apache Cassandra): is a scalable, highly available, and managed Apache Cassandra–compatible database service. Apache Cassandra is a free and open-source, distributed, wide column store, NoSQL database management system designed to handle large amounts of data across many commodity servers, providing high availability with no single point of failure. 


# Bash

- grep: filter matches only from output:
	grep 'blabla' -o file.log

- Regex in grep:
	grep -E 'REGEX' file.log

- uniq: filter unique row (delete duplicate only, so could be usefull with 'sort' cmd)
	less file.log | sort | uniq


# Hardware

- SSD SATA (Serial ATA): connection from SSD to different hardware (pc or laptop, old or new)

- SSD PCIe (Peripheral Component Interconnect Express): direct connection from SSD to motherboard. A lot more faster (used by graphical card too). Use more energy.


# Network

- Tunneling Protocol: is a communications protocol that allows for the movement of data from one network to another. It involves allowing private network communications to be sent across a public network (such as the Internet) through a process called encapsulation.
	Because tunneling involves repackaging the traffic data into a different form, perhaps with encryption as standard, it can hide the nature of the traffic that is run through a tunnel.

- SSH: the concept of agent forwarding and proxy jump ([resource](https://smallstep.com/blog/ssh-agent-explained/)). It consists in use local ssh-agent in a ssh connection to a remote host, so 2 channels open from local to remote hosts, 1 for ssh interaction and 1 for the ssh-agent. In this way user can use it's local keychain from the remote host itself. The agent forwording can be started on demand (ssh -A ...) or, in .ssh/config, started by default. There are security problems using this over a bastion host to reach a different remote host (since a root user in bastion host can use the agent forwarding for steal keychain of a ssh session of another user), so the best way it's: 
	1. Put ssh-agent under password
	2. Use ProxyJump, in this way the ssh session will be from your local workstation and not throught a bastion host


# Software

- Barrier: is software that mimics the functionality of a KVM switch, which historically would allow you to use a single keyboard and mouse to control multiple computers by physically turning a dial on the box to switch the machine you're controlling at any given moment. 
	Barrier does this in software, allowing you to tell it which machine to control by moving your mouse to the edge of the screen, or by using a keypress to switch focus to a different system.

## Chat

- Internet Relay Chat (IRC): is an application layer protocol that facilitates communication in the form of text. The chat process works on a client/server networking model.

## SW Pattern

- Facade pattern: is a software-design pattern commonly used in object-oriented programming. 
	Analogous to a facade in architecture, a facade is an object that serves as a front-facing interface masking more complex underlying or structural code

# TOOL

- Asciinema https://asciinema.org/: Record and share your terminal sessions, the right way.

- Nginx: versatile HTTP server and reverse proxy / load balancer / HTTP cache / mail proxy.






