🧠 Brain Tasks App – CI/CD Deployment on AWS
This project demonstrates the deployment of a React.js application to a production-ready state. The architecture leverages Docker for containerization and a full AWS DevOps stack for automated orchestration.

💻 Application Details
App Name: Brain Tasks App

Tech Stack: ⚛️ React.js

Source Code: GitHub Repository

Exposed Port: 🚪 3000

🛠️ Tools & AWS Services Used
🐳 Docker: Containerization of the React environment.

📦 AWS ECR: Private registry for storing Docker images.

☸️ AWS EKS: Managed Kubernetes service for orchestration.

🏗️ AWS CodeBuild: Automated building and testing of code.

🚀 AWS CodeDeploy: Automated deployment to the EKS cluster.

🔗 AWS CodePipeline: Continuous Integration/Continuous Delivery (CI/CD).

🛡️ Amazon CloudWatch: Centralized logging and monitoring.

🐙 GitHub: Version control and source management.

🚀 Project Workflow
1️⃣ Clone the Repository
Bash

git clone https://github.com/Vennilavan12/Brain-Tasks-App.git
cd Brain-Tasks-App
2️⃣ Dockerize the App
Create a Dockerfile to package the application and its dependencies.

3️⃣ Push Docker Image to ECR
Authenticate and push the built image to the Amazon Elastic Container Registry.

4️⃣ Kubernetes Deployment on AWS EKS
Configure your local environment to interact with the cluster:

Bash

aws eks update-kubeconfig --region ap-south-1 --name darwin-cluster
kubectl get nodes
5️⃣ Apply Manifest Files 📄
Deploy the application and expose it via a LoadBalancer:

Bash

kubectl apply -f deployment.yml
kubectl apply -f service.yml
6️⃣ CI/CD Pipeline Setup 🔄
CodeBuild: Compiles the code and creates the image.

CodeDeploy: Manages the rolling update on EKS.

CodePipeline: Orchestrates the entire flow from "Git Push" to "Live."

7️⃣ Monitoring & Logging 📊
Integrate CloudWatch to track build status, deployment logs, and application health.
