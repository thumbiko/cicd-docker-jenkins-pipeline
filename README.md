# CI/CD Pipeline for Dockerized Python Web Application

An automated end-to-end pipeline that builds, tests, and deploys a Python Flask application using Jenkins and Docker on AWS.

## 🚀 Architecture


* **Version Control:** GitHub
* **CI/CD Tool:** Jenkins (Pipeline-as-Code)
* **Containerization:** Docker
* **Web Server:** Nginx (Reverse Proxy)
* **Cloud Platform:** AWS EC2 (Ubuntu)

## 🛠️ Project Structure
├── app/                # Python Flask application
├── tests/              # Unit tests
├── Dockerfile          # Container configuration
├── Jenkinsfile         # CI/CD Pipeline definition
└── nginx.conf          # Nginx reverse proxy setup

## ⚙️ How it Works
1. **Trigger:** Developer pushes code to the `main` branch.
2. **Build:** Jenkins pulls the code and builds a new Docker image.
3. **Test:** Automated Python unit tests run inside the container.
4. **Deploy:** Jenkins pushes the image to Docker Hub and updates the container on the AWS EC2 instance.
5. **Access:** Nginx routes traffic from Port 80 to the Docker container.

## 🔧 Setup Instructions
1. Install Jenkins on your EC2 instance.
2. Configure Docker and Git on the Jenkins server.
3. Add your DockerHub and AWS credentials to Jenkins.
4. Create a 'Pipeline' job and link it to this repository.
