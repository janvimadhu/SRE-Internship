# Tasks:
   
# Docker Task

Assignment:

1. Using alpine as a base Docker image, write a docker file that configures nginx and serves hello world static page.
2. Create an nginx proxy that routes the requests to the above docker container.

# Network Task 

1. Set up two focal VMs and assign IPs from the same network range eg.172.16.0.0 /24 and check if ping works.
2. Add another focal VM to the setup and assign connectivity in the following order where VM2 acts like a router. VM1 <->VM2<->VM3. VM1 should be from 172.16.0.0 /24 and VM3 should be from 192.168.0.0 /24. Should be done using static routing. 
3. Assign IPs to loopback (lo interface) and recreate #1 and #2 via BGP using FRR. VM1 lo: 10.1.1.1/32, VM2 lo: 10.1.1.2/32, VM3 lo: 10.1.1.3/32. Ping should work between the loopback addresses. The network range for BGP IPs is 172.16.0.0/24 for both the scenarios. 

# SSH-ng Task

1. What is encryption & decryption? Types of encryption.
2. What is a Certificate Authority, Intermediate CA, Server & Client cert?
3. Generate a self-signed client certificate using OpenSSL with Root CA certs, Intermediate CA certs, Server and client certificates, and attach the steps that you used to generate it. Attach the final certificates that you have generated.
4. How does SSH work?
5. What is key forwarding in SSH? How do you forward keys? Mention a use case.
6. What is agent forwarding in SSH? How do you perform agent forwarding with SSH?  Mention a use case.

# Inventory Management Task

1. What is PXE?
2. What are virtual machines, What is the value add that they provide, at least mention 3 use cases?

# Git

Task-1:
Create git repo and host it on any public git hosting service [github / gitlab / bitbucket]
Clone that repo , create a branch, add a Readme file and push the changes to branch and get it merged by your mentor
( Verify if it has reflected on UI and attach screenshot as solution )

Task-2:
Simulate a merge conflict and try to resolve it.
( Share the steps as a solution)

Task-3:
Create 2 Git repositories, Project-A with Readme file and Project-B empty repository. Write a script to pull the latest changes from Project-A/Readme file and push it to Project-B/Readme with a proper commit message each time there is a change.
Additionally if you want the pull the latest changes from A to B periodically how would you do it (Explore various ways you can achieve this and implement anyone)
( Share the scripts as solution ) 
