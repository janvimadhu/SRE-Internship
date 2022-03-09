# Day1-Task

STEP 1: Build the Docker IMAGE 

Use the command , docker build -option <name-of-the-image> <path-to-the-dockerfile-directory>
  
For example : Let the command be: 
  
  docker build -t day1task .
  
        Here, docker build is the basic command to build the docker image 
  
        -t option flag tags our image 
  
        day1task is the name of the image which we have to refer when we run the container
  
        . at the end of the docker build command basically informs that the dockerfile should look for the dockerfile in the current directory. 
  
  Now your Docker image is ready , Let's run our application. 


STEP 2: RUN THE DOCKER IMAGE TO START THE CONTAINER 
  
  To run the container , we use the docker run command 
  
  The syntax be - docker run -options <port-map> <name-of-the-created-image>
  
  Example: docker run -d -p 80:80 day1task
  
          Here , -d -p are the options which ensures that the new container is in detached mode and the mapping between the host port and the container port is created.
  
          80:80 refers to the host port:container port(tcp) .
  
          Now go and run your application at http://localhost:80 
  
  

OUTPUT:

![image](https://user-images.githubusercontent.com/74037593/152694088-724ab549-5829-455e-ae1a-c50cbb89a686.png)

![image](https://user-images.githubusercontent.com/74037593/152694120-70002b4a-948e-4d8a-b40b-89c4ad67eee1.png)


