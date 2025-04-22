# 📦 Kubernetes Deployment

A complete backend system for managing instructors, built entirely from scratch with **Java 17** and **Spring Boot**, containerized and deployed on a local **Kubernetes (Minikube)** cluster.

------------------------------------------------------------

## 📖 Project Description

This project was developed by **Mohamad Shosha** from scratch as a full backend system integrated with a **MySQL 8** database.  

I personally:
- Designed and built the **backend application using Java & Spring Boot**.
- Created the **Dockerfile** for containerizing the application.
- Wrote a **Docker Compose file** to test and run the application and database locally before Kubernetes deployment.
- Published the backend application Docker image on **Docker Hub**.
- Created all **Kubernetes deployment and service YAML files** manually.
- Pulled the published image from Docker Hub via Kubernetes.
- Deployed both the backend app and the database on **Minikube**.
- Exposed the backend service via **LoadBalancer type service** on a random Minikube NodePort.

This project demonstrates a clean, independent, and integrated DevOps workflow handled entirely by me.

------------------------------------------------------------

## 📁 Project Structure

- mysql-deployment.yaml  
- mysql-service.yaml  
- app-deployment.yaml  
- app-service.yaml  
- Dockerfile  
- docker-compose.yaml  
- README.md

------------------------------------------------------------

## 🛠️ Technologies & Tools

- Java 21  
- Spring Boot  
- MySQL 8  
- Docker  
- Docker Compose  
- Docker Hub  
- Kubernetes (Minikube)  
- YAML  

------------------------------------------------------------

## 🚀 How to Run This Project

**1️⃣ Start Minikube:**

minikube start

**2️⃣ Deploy the MySQL Database:**

kubectl apply -f mysql-deployment.yaml  
kubectl apply -f mysql-service.yaml  

**3️⃣ Deploy the Instructor Management Application:**

kubectl apply -f app-deployment.yaml  
kubectl apply -f app-service.yaml  

**4️⃣ Expose the Application:**

minikube service instructor-service  

➡️ This command will open your app in the browser using a random localhost port.

------------------------------------------------------------

## 🌐 Service Details

- **MySQL Service:**  
  Internal ClusterIP service exposing MySQL on port **3306**.

- **Instructor Service:**  
  LoadBalancer service exposing the Spring Boot application.  
  The application listens on **container port 8080** and is exposed via **NodePort (random Minikube port)**.

To get the accessible URL:  
`minikube service instructor-service`

------------------------------------------------------------

## 🗄️ Database Connection Configuration (inside app)

- **URL:** jdbc:mysql://mysql:3306/mydb  
- **Username:** root  
- **Password:** Nmnmnm6@@

------------------------------------------------------------

## 🎯 Purpose of This Project

This project is designed to:

- Practice **Java & Spring Boot backend development**.
- Build and run **Docker containers** for backend applications and databases.
- Use **Docker Compose** for multi-container orchestration locally.
- Publish Docker images to **Docker Hub**.
- Deploy Docker images using **Kubernetes** with manually written YAML configurations.
- Expose services through Kubernetes **LoadBalancer**.
- Simulate a production-like environment for backend service orchestration.

------------------------------------------------------------

## 👨‍💻 Author & Contact

**Name:** Mohamad Shosha  
**Email:** moshosha267@gmail.com  
**Phone:** +20 107 065 8742  
**GitHub:** https://github.com/Mohamad-shosha  

------------------------------------------------------------

⭐ If you find this project useful, feel free to star it and share it!
