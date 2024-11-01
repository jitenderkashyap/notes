# How to use Docker 
## Step 1
`` docker pull imagename ``
## Step 2
#### Create Dockerfile in current directory and paste code
`` 
FROM node:latest
COPY index.js index.js
EXPOSE 3000
CMD [ "node","index.js" ]
``
## Step 3
#### Build image using below command
`` docker build -t imagename . ``

`` 
***imagename*** indicates your custom image name 
***.*** indicates Dockerfile exists in your current location 
``

## Step 4
#### Run container
``
docker run -it -p 3000:3000 imagename
``