# Learning Platform Demo

A 3-tier containerized learning platform application.

## Architecture

- **Frontend**:
   React.js , 
   Runs inside a Kubernetes Deployment , 
   Exposed via a NodePort service , 
   Internal Container Port: 80 , 
   External NodePort: 30081
  
- **Backend**:
   Python FastAPI , 
   Communicates with PostgreSQL inside the cluster , 
   Exposed through a NodePort service , 
   Internal Container Port: 8000 , 
   External NodePort: 30080
  
- **Database**:
   PostgreSQL , 
   Exposed internally via a ClusterIP service only (no external access) , 
   Port: 5432

## Kubernetes Components Used
  - **Deployments**: (frontend, backend, database) , 
  - **Services**: NodePort (frontend & backend) ClusterIP (database)

  

## Features

- View all courses 
- Add new courses
- Delete courses
- RESTful API

## Running the Application
-**Apply all manifests**
  kubectl apply -f k8s/  (Change the path according to where your YAML files are located)
-**Check pods**
  kubectl get pods
-**Check services**
  kubectl get svc
  
## Access

- Frontend: http://<Node-IP>:30081
- Backend API: http://<Node-IP>:30080
- API Docs: http://<Node-IP>:30080/docs

## Database Credentials

- Database: learning_platform
- User: admin
- Password: admin123
