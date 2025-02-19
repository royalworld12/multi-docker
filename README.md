# Multi Container Docker Setup

This project demonstrates how to create a multi-container Docker environment using Docker Compose. It defines and manages two services:

Web Service (Node.js application): A simple Node.js application that communicates with a MongoDB database. It serves as the front-end or API server in this environment.

Service Worker (Node.js application) : A simple Node.js application where calculation is done and it operates with redis to watch out.

Database Service (Postgres): A Postgres database that stores and retrieves data for the Node.js application. The database is running inside a separate container and is easily configurable and scalable.

This setup allows for efficient isolation of services, improved scalability, and easier management of the different components of the application. With the use of Docker Compose, you can easily configure, build, and run multi-container Docker applications, making it an ideal solution for both development and production environments.


## Installation

Installation Procedure for client
```bash
 cd complex/client
  npm install
```


Installation Procedure for Service
```bash
 cd complex/service
  npm install
```

Installation Procedure for Worker
```bash
 cd complex/worker
  npm install
```

If you are using Docker than you can use. All the application will start running in docker.

```bash
 docker-compose up --build
```
    
