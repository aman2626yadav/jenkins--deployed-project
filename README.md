# jenkins--deployed-project 
Hello folks!
In this project, we deploy a web application using Jenkins CI/CD, AWS EC2, Docker, and ArgoCD in a simple and practical way. here are some screenshot 
steps to do it
 1. Launch an EC2 instance (Amazon Linux or Ubuntu).
   Open required ports in the security group:
  8080 → Jenkins
  80 / 443 → Web Application
 Connect to the EC2 instance using SSH.

 2. Install Jenkins on EC2
   Update the system packages.
   Install Java (Jenkins dependency).
   Install Jenkins.
  Start and enable Jenkins service.
  Access Jenkins in browser:

3. Install Docker on Jenkins Server
   Install Docker on the same EC2 instance.
   Start and enable Docker service.
   Add Jenkins user to Docker group so Jenkins can run Docker commands. 
   Verify Docker installation

4. The Jenkins pipeline performs the following tasks:
   Clone source code from GitHub
   Build application
  Create Docker image
  Push Docker image to Docker Hub (or any registry)
  clean old builds and containers
  
  GitHub → Jenkins (CI) → Docker Image → ArgoCD (CD) → Kubernetes → Live Application


