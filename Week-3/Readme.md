# DB Basics - Mariadb , Galera

MariaDB Version to be used: 10.5.13
Backup Method should be Physical(mariabackup).

1. Setup Master-slave Replication b/w two mysql server.

2. Setup a Galera cluster with 3 nodes on version 10.5.13 and the sst method should be mariabackup. 

3. A sql file is attached, that has the nginx logs in a table, you will have to restore on the above setup and provide the below asked information.
     
Use MariaDB Queries to provide the stats below

        a. summary for the day/week/month:
                highest requested host
                highest requested upstream_ip
                highest requested path (upto 2 subdirectories ex: /check/balance)
        b. total requests per status code (Ex: count of requests returning 404/401/502/504/500/200)
        c. Top requests
                top 5 requests by upstream_ip
                top 5 requests by host
                top 5 requests by bodyBytesSent
                top 5 requests by path (upto 2 subdirectories ex: /check/balance)
                top 5 requests with the highest response time
                get top 5 requests returning 200/5xx/4xx per host
        
        d. find the time last 200/5xx/4xx was received for a particular host
        e. get all request for the last 10 minutes
        f. get all the requests taking more than 2/5/10 secs to respond.
        g. get all the requests in the specified timestamp (Ex: from 06/Mar/2021:04:48 to 06/Mar/2021:04:58)
        h. Create partitioning on this table using the time values, the table should have weekly partitions.
        i. Truncate the partitions from week 21 to 25;
     
     
# Azure


All resources must be created in India Regions.
1. Create a Resource Group (using portal)
2. Create a vnet/subnet inside the resource group (using portal)
3. Create a virtual machine OS: Ubuntu Focal (using portal). Explore Availability sets/zones.
4. Setup a Flask app inside the VM which prints the hostname of the VM
5. Create an SP with Contributor access on the subscription.
6. Create a VM in the same resource group, vnet, subnet using terraform using the SP in step 5 and setup the flask app in the second VM as well
7. Add an NSG rule to allow inbound traffic only on ssh port and the port on which the flask app is running (using portal)
8. Create a load balancer, to balance between the 2 VMs (flask app), so that it prints the hostnames of both the VMs in round robin.
9. Shut down one of the machines and check how the load balancer works.
10. Add a 10G data disk to the machine, and create a mount point to redirect the flask app logs to the mount point. Explore disk redundancy options.
11. Resize the VMs (via portal and terraform resp.)
12. Destroy all the resources. Delete the SP and extra users added if any.


# Aerospike

Aerospike:
     
     Install and configure 1 node Aerospike cluster community edition
     The AS cluster should have a username/password
     Data should be persisted on disk
     Add 2 more nodes to the cluster without restarting AS service on first one
     Create a namespace Orders

Testing:

     Write a program using an AS client to write and read the data from AS
     The namespace should have the following sets (buyer details, product details)
     Each set should have 3000 records.
     The records should have an expiry of 24h


# Proxy

- Create a self signed wildcard certificate with domain *.intern.phonepe.in with expiry validity of 2 years.
- Setup a simple server running on port 5440 that implements ping/pong requests
- Using certificates from step 1, setup a nginx ssl proxy (domain ping.intern.phonepe.in) running on port 444. Proxy should redirect request to the locally setup ping-pong server

testing of the setup:
try hitting https://ping.intern.phonepe.in expected response should be:

     pong
     
  
     
