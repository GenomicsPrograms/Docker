# Docker
Docker containers are created by using a combination of Dockerfile + image. 

<b>Find the right image</b>
1. Visit any docker repository and search for the image that's right for your project. 
   Then use docker to pull it into your environment.

   <code>docker pull repoName/imageName</code>
   
2. In the linux command line type the following to view the pulled image.
   
   <code>docker images</code>

3. Open a bash shell on the image or to run R on the command line and check it contents and capabilities.
   Note: The image must be R based for the second line of code to work.

   <code>docker run -ti repoName/imageName bash</code><br>
   <code>docker run -ti repoName/imageName R</code>
   
<b>Create a Dockerfile</b>

4. Create a Dockerfile, this repo has examples that you can review. The image that you choose is always 
   the first line in your Dockerfile, for example see below:
   
   <code>FROM debian:testing</code>
   
   or
   
   <code>FROM ubuntu:16.04</code>
   
 <b>Build your Docker container</b>
 
 5. After creating your Dockerfile and specifying the right image within it, build your container.
 
         docker build -f Dockerfile -t dinulabasu/potra_cor:2.0 .
 
