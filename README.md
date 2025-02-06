# devops-assignment

# Running the App Locally
# Install Docker
Ensure Docker is installed on your local machine.

# Check Docker Version
docker --version

# Install Docker (If Not Installed)

# Option 1: Build & Run Locally
docker build -t hello-world-app .
docker run -p 5000:5000 hello-world-app
# open http://localhost:5000 in your browser.

# Option 2: Pull & Run from DockerHub
docker pull your-dockerhub-username/hello-world-app:latest
docker run -p 5000:5000 your-dockerhub-username/hello-world-app:latest

# Check
docker ps


# Triggering the CI/CD Pipeline
The pipeline automatically runs when changes are pushed to the master branch.

# Steps to Manually Trigger the Pipeline

    Make changes to the repository.
    Commit and push the changes:

git add .
git commit -m "Updated application"
git push origin master

Go to GitHub → Actions Tab.
Monitor the workflow run.


# Rollback steps
Rollback to Previous Deployment

kubectl rollout undo deployment hello-world

kubectl rollout status deployment hello-world


