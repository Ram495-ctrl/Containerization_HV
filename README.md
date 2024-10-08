<h1> Graded Assignment on Dockerizing a Plain HTML Page With Nginx 
<h1> Dockerized Nginx Serving HTML <h1>

This project contains a simple HTML page served using Nginx in a Docker container.

<h1> Files <h1>
  
index.html

A plain HTML page with the content "Hello, Docker! by Rama Srinivas".

nginx.conf

An Nginx configuration file that serves the index.html page and listens on port 81.

Dockerfile

A Dockerfile that defines the Docker image. It uses an official Nginx base image, copies the index.html and nginx.conf files into the container, and ensures that the Nginx server is started when the container is run.

Building the Docker Image

To build the Docker image, run the following command in the terminal:


<h1> Steps to Build and Run <h1>

1. Build the Docker image:

docker build -t nginx-html .

![nginx build](https://github.com/user-attachments/assets/763e2896-7744-41c6-95f6-5f353d8f03a7)


2. Run the container locally:

![docker_image](https://github.com/user-attachments/assets/1992f83f-d0fe-4be0-a191-374f50fa873a)

3. Checking the Nginx with EC2 ip address:

add ports :

![ports](https://github.com/user-attachments/assets/6640c732-abec-4dc1-b8df-9f72097d8808)

![docker_compose_ip](https://github.com/user-attachments/assets/13eab417-e91b-4d2d-b756-ce2b4aab447f)

![docker_compose_ip_https](https://github.com/user-attachments/assets/4b3db4c4-e7b8-4fe0-aa1a-1a22dcad4061)

Visit (https://35.84.179.79:444/)/ to see the HTML page in action.



