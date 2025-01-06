Assignment App Deployment Guide
Overview
This repository contains the code for a containerized 3-tier application that includes:

Frontend: A user interface to input goals.
Backend: The API that stores and retrieves goals from a database.
Database: MongoDB to store the goals data.
The app is containerized using Docker, orchestrated with Docker Compose, and deployed using a CI/CD pipeline in Jenkins.

Prerequisites
Docker: Make sure Docker is installed on your machine.
Docker Compose: Required to orchestrate the containers.
Jenkins: Jenkins should be set up for the CI/CD pipeline.
Setting Up the Application

1. Clone the Repository
   Clone the project repository to your local machine:

git clone https://github.com/FouedNasser/assignement-app.git
cd assignement-app 2. Environment Setup
Backend Environment Configuration
In the root directory of the repository, create a .env file for the backend with the necessary environment variables. Example:

BACKEND_PORT=5000
MONGO_URI=mongodb://mongo:27017/assignement-db
MongoDB Configuration
Create a .env file for MongoDB configuration in the root directory of the repository:

MONGO_INITDB_ROOT_USERNAME=admin
MONGO_INITDB_ROOT_PASSWORD=password 3. Build and Run the Application
Using Docker Compose, you can easily build and run the application:

docker-compose up -d --build
This command will:

Build the images for the backend, frontend, and MongoDB.
Start the services in detached mode. 4. Accessing the Application
Once the services are up and running, you can access the application:

Frontend: http://localhost:3000
Backend API: http://localhost:5000 5. Stopping the Application
To stop the running containers, use:
docker-compose down
