Created by Kaushal Kishore <br>
Email : kaushal.rahuljaiswal@gmail.com<br>
Website : http://www.kaushalkishore.com<br>

<h2>Dockerfile for creating an apache2 docker image</h2>

<h4>Steps for creating image from the Docker-Apache2:</h4>

<b>Step 1 :</b> Clone the Docker-Apache2.git
<pre>
Command: 
git clone https://github.com/kaushalkishorejaiswal/Docker-Apache2.git
</pre>

<b>Step 2 :</b> Change the directory to the clone folder
<pre>
Command:
cd Docker-Apache2
</pre>

<b>Step 3 :</b> Create the Docker Image
<pre>
Command: 
sudo docker build -t <NAME_OF_YOUR_DOCKER_IMAGE>
</pre>

<pre>
<b>Note : </b>
  a). This command will be fired where the DockerFile will be placed
  b). <NAME_OF_YOUR_DOCKER_IMAGE> : Replace it with your image name
</pre>

<b>Step 4 :</b> Create an Apache Installed Container from the image
Command Syntax: 
sudo docker run -name [container name] -p [port to access (New Port):port exposed(original port)] -i -t [image name]
<pre>
Command:
sudo docker run --name <NAME_OF_YOUR_DOCKER_CONTAINER> -d -p 8082:80 <NAME_OF_YOUR_DOCKER_IMAGE>
</pre>

<b>Step 5 :</b> Now you can access your apache container from your web browser.
<pre>
Command:
http://127.0.0.1:8082/
</pre>

<h4>Some other important commands:</h4>
<ul>
<li>docker images : To list all the images of your docker</li>
<li>docker ps : To list all the runing containers</li>
<li>docker kill <CONTAINER_NAME> : To kill the runing container</li>
<li>docker rm <CONTAINER_NAME> : To delete the container from the system.</li>
</ul>
