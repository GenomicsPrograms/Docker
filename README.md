# Docker
Docker containers are created by using a combination of Dockerfile + image. 

<b>Find the right image</b>
1. Visit any docker repository and search for the image that's right for your project. 
   Then use docker to pull it into your environment.

   <code>docker pull repoName/imageName</code>
   
2. In the linux command line type the following to view the pulled image.
   
   <code>docker images</code>

3. Check out the image.

   <code>docker run -ti repoName/imageName bash</code>

