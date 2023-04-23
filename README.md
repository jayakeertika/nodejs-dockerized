# nodejs-dockerized

# Building your image
docker build . -t jaya/nodejs-dockerized

## Run the image ##
docker run -p 49160:8080 -d jaya/node-web-app 

Print the output of your app:
// Get container ID   
    $ docker ps

// Print app output   
    $ docker logs <container id>

// Example   
    Running on http://localhost:8080

// Enter the container   
    $ docker exec -it <container id> /bin/bash

# Testing your Application 
docker ps      
    CONTAINER ID   IMAGE                    COMMAND                  CREATED          STATUS          PORTS                    NAMES
    0ba95eb7388d   jaya/nodejs-dockerized   "docker-entrypoint.s…"   25 seconds ago   Up 24 seconds   0.0.0.0:4900->8080/tcp   dazzling_colden

curl -i localhost:49160  
HTTP/1.1 200 OK    
X-Powered-By: Express    
Content-Type: text/html; charset=utf-8    
Content-Length: 11     
ETag: W/"b-Ck1VqNd45QIvq3AZd8XYQLvEhtA"    
Date: Sun, 23 Apr 2023 01:22:09 GMT    
Connection: keep-alive    
Keep-Alive: timeout=5    

Hello World                                     
