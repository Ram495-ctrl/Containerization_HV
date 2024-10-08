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



3. Checking the Nginx with EC2 ip address:

add ports :

![ports](https://github.com/user-attachments/assets/6640c732-abec-4dc1-b8df-9f72097d8808)

<img width="475" alt="image" src="https://github.com/user-attachments/assets/d12a21de-c781-467c-98ff-c3423a64fc72">


![docker_compose_ip_https](https://github.com/user-attachments/assets/4b3db4c4-e7b8-4fe0-aa1a-1a22dcad4061)

Visit https://35.84.179.79:444 to see the HTML page in action.

<h1> Pushing the Image to Amazon ECR <h1>

Login to ECR:

```
aws ecr get-login-password --region us-west-2 | docker login --username AWS --password-stdin 975050024946.dkr.ecr.us-west-2.amazonaws.com
```

<h1> Generate Certificates <h1>

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt

