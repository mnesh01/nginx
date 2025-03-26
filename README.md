## Nginx Load Balancer with Node.js Cluster

An Nginx reverse proxy to load balance multiple Node.js instances running in Docker containers. The goal is to efficiently distribute incoming traffic among multiple backend servers to ensure high availability and better performance.

## Technologies used 

Nginx (Reverse Proxy & Load Balancing)

Node.js (Backend Servers)

Docker & Docker Compose (Containerization)

JavaScript

## Setup & Installation

1. Clone the Repository
   
git clone https://github.com/mnesh01/nginx.git

cd nginx

2. Build and Run with Docker
   
docker-compose up --build

3. Access the Application

Once the containers are up, visit:
 http://localhost:80

## Configuration details

Nginx Configuration (nginx.conf):

Uses least_conn strategy to distribute traffic.

Forwards requests to Node.js servers running on 127.0.0.1:3001, 127.0.0.1:3002, 127.0.0.1:3003.

Uses server_name localhost (modify if hosting externally).

Node.js Server (server.js):

Each instance runs a basic Express server on different ports:

## Scaling the App
If you need to scale up, modify docker-compose.yaml by adding more Node.js services and updating nginx.conf.
