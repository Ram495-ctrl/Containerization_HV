<h1> Graded Assignment on Dockerizing a Plain HTML Page With Nginx 
<h1> Dockerized Nginx Serving HTML <h1>

This project contains a simple HTML page served using Nginx in a Docker container.

<h1> Files <h1>
index.html

A plain HTML page with the content "Hello, Docker! by Rama Srinivas".

nginx.conf

An Nginx configuration file that serves the index.html page and listens on port 80.

Dockerfile

A Dockerfile that defines the Docker image. It uses an official Nginx base image, copies the index.html and nginx.conf files into the container, and ensures that the Nginx server is started when the container is run.

Building the Docker Image

To build the Docker image, run the following command in the terminal:
