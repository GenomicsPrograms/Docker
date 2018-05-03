# Docker
Docker containers are created by using a combination of Dockerfile + image. 

<b>Find the right image</b>
1. Visit any docker repository and search for the image that's right for your project. 
   Then use docker to pull it into your environment.

       docker pull repoName/imageName
   
2. In the linux command line type the following to view the pulled image.
   
       docker images

3. Open a bash shell on the image or to run R on the command line and check it contents and capabilities.
   Note: The image must be R based for the second line of code to work.

       docker run -ti repoName/imageName bash
       docker run -ti repoName/imageName R
   
<b>Create a Dockerfile</b>

4. Create a Dockerfile, this repo has examples that you can review. The image that you choose is always 
   the first line in your Dockerfile, for example see below:
   
       FROM debian:testing
   
   or
   
       FROM ubuntu:16.04
   
 <b>Build your Docker container</b>
 
 5. After creating your Dockerfile and specifying the right image within it, build your container.
    This is also known as the debugging step, as Docker will point out the errors.
 
        docker build -f Dockerfile -t repoName/imageName:latest .
 
 <b>Use your Docker container</b>
 
 6. Open your Docker container and mount your folder within it.
 
        docker run -i -t -v /home/user/:/user/ repoName/imageName:latest /bin/bash

 <b>Push your Docker container </b>
 
 7. Once you are happy with your container, it's time to push it to your docker hub repo.
    First you need to login to your docker hub repo.
    
        docker login
        docker push repoName/imageName:latest
 
 
 
