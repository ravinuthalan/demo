# demo

# Workflow
Modify a static web page content in VS Code
Save and check in to git
Push to github
This triggers Jenkins pipeline via webhook
Pipeline script is also saved in repo as Jenkinsfile
Pipeline checks out code
Builds docker image which deploys static web page onto latest ngnix and makes it available on port 80
Pushes docker image to docker hub using credentials defined in Jenkins

# Testing
Pull the latest image from docker hub
Create a container 
Open the web page to see the changes reflecting
