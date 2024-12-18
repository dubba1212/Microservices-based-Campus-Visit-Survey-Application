# Microservices-based Campus Visit Survey Application

## Overview
This project demonstrates the deployment of a full-stack application using Spring Boot for the backend, Angular for the frontend, and AWS services for hosting and orchestration. CI/CD is implemented with Jenkins and Docker.

## Table of Contents
1. Environment Setup
2. Technologies Used
3. Installation Guide
4. Angular
5. Spring Boot
6. MySQL RDS Setup
7. Deployment
8. EC2 Instances
9. Rancher Setup
10. Jenkins Setup
11. CI/CD Pipeline
12. Testing
13. Future Enhancements

## Environment Setup
#### Development Tools
- Visual Studio Code: For Angular development
- Eclipse EE: For Spring Boot development
- MySQL Workbench: For database management and queries
#### Frameworks and Dependencies
- Spring Boot: RESTful Web Services
- Angular: Frontend application development
- JPA: For database communication
- Docker: For containerizing applications

### Technologies Used
AWS: EC2, RDS, and Rancher for orchestration
Jenkins: For CI/CD pipeline
Docker Hub: Hosting Docker images
MySQL: Database setup on AWS RDS

## Installation Guide
### Angular
1. Install Node.js from [Node.js](https://nodejs.org).
2. Install Angular CLI:
``` bash
npm install -g @angular/cli
```
3. Create a new Angular project:
``` bash
ng new angular
```
4. Install Bootstrap for styling:
```bash
npm install 
```
5. Generate components:
```bash
ng generate component home
ng generate component survey
ng generate component allsurveys
```
6. Launch the development server:
``` bash
ng serve
```
Navigate to http://localhost:4200.
### Spring Boot
1. Generate a new Spring Boot project from start.spring.io with the following dependencies:
- Lombok
- Spring Web
- MySQL Driver
- Spring Data JPA
2. Package the application using Maven:
```bash
mvn clean package
```
### MySQL RDS Setup
1. Log into AWS and navigate to RDS.
2. Create a MySQL instance and configure credentials.
3. onnect to the database using MySQL Workbench.
## Deployment
### EC2 Instances
1. Launch Ubuntu 20.04 EC2 instances.
2. Install Docker on each instance:
bash
Copy code
sudo apt update  
sudo apt install docker.io  
3. Create a security group allowing traffic on ports 8080, 80, 443, and 22.
### Rancher Setup
1. Navigate to the Rancher dashboard and create a custom cluster.
2. Deploy the Docker image to the cluster.
### Jenkins Setup
1. Install Jenkins on a new Ubuntu EC2 instance:
bash
Copy code
sudo apt update  
sudo apt install openjdk-11-jdk  
sudo apt install jenkins  
2. Configure Jenkins with a GitHub webhook for automatic builds.
### CI/CD Pipeline
1. Create a Jenkins pipeline linked to your GitHub repository.
2. Configure the pipeline to build and push Docker images to Docker Hub.
3. Set up Rancher to deploy updated images from Docker Hub.
### Testing
- Frontend: Testing with Angular CLI.
- Backend: Postman API tests.
- Database: SQL queries in MySQL Workbench.
### Future Enhancements
1. Integrate monitoring tools like Prometheus and Grafana.
2. Automate scaling with Kubernetes.
3. Implement advanced security measures like AWS IAM policies.
## Conclusion
This project demonstrates the integration of modern DevOps practices with cloud infrastructure to deploy a scalable and reliable web application.