# Nginx & Traefik

    Machine 1: Over a container, setup a server serving an api /howareyou
    Machine 2: Setup a server using nginx that serves as front (reverse proxy) to container running in machine 1 
    
    Proxy server should return request for /howareyou when queried



# Big data/distributed systems intro and zookeeper
  
     1. Set up a zookeeper cluster with 3 nodes. Use below link to download the compiled binaries.Use version Apache ZooKeeper 3.6.3. https://zookeeper.apache.org/releases.html
     2. How to Identify which zookeeper is the leader?
     3. How to identify the connections on a zookeeper node?
     4. What will happen if the leader goes down?
     5. What will happen if you purge snapshot?
     6. What will happen if you add 1gb znode?
