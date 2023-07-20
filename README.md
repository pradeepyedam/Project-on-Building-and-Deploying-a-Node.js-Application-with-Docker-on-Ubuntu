Building and Deploying a Node.js Application with Docker on Ubuntu

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/87c108d2-b07b-4b9b-a07f-36822502d280">
<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/f3b3ac9c-5fc6-4cc9-905b-c79e701738d2">

Step 1 - Installation of docker on Ubuntu The first step is to update the package manager. The second step is to install Docker by using the command "sudo apt-get install docker.io -y" on the terminal. After installation, the Docker version can be checked by typing "sudo docker –version" in the terminal. Command-

1.apt-get update

2.apt-get install docker.io -y

3.docker --version

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/a1d6fe45-16eb-4cd1-bb26-b1411e9a191b">

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/92a0f0b7-08dc-4b7b-8634-36b8c5698d97">

Step 2 : Clone the code from Github The code for the project is cloned from GitHub using the command 'git clone <repository_url>'. In this case, the repository URL is https://github.com/LondheShubham153/node-todo-cicd.git

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/3854bdcd-937e-458e-965d-1bc6ac421879">

(Here I’m cloning the code from Shubham londhe’s account and even you can forks that Repositorie to your github account).

Step 3: Check the files and understand the requirements Check the files and understand the requirements Once the code has been cloned, we navigate to the directory using the command 'cd react_django_demo1_app' and use the 'ls' command to list the files in the directory. This helps us to understand the requirements of the project. Commands

Cd react_django_demo1_app

ls

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/0901f459-412a-40fd-be4c-85df852342fa">

In the README.md file, the user can find the requirements for the project. After understanding 'README.md' file the requirements for the project are documented, including the need for Node.js, Java, and npm.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/4fa513c8-ffa0-4186-8dde-2427585c298c">

Step 4: Create a docker image using a dockerfile

To Create a Docker image using a Dockerfile A Dockerfile is used to define the configuration of the Docker image. In this step, a Dockerfile is created to build the Docker image for the project. I suggested to use base image the node image version 19-alpine3.16 from the Docker Hub. The Alpine Linux distribution is a lightweight Linux distribution that is commonly used in Docker images because of its small size. The 19-alpine3.16 tag refers to a specific version of the image.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/cbe83cfd-3dd5-4893-a9d8-aae18ab55427">

Create a Dockerfile to define the environment for the application. The Dockerfile specifies the base image to use, the packages to install, and any other configuration required for the application.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/1bf43b2a-8fa7-4897-993c-ac92ac89636e">

Step 4: Build the docker image Build the Docker image Once the Dockerfile has been created, the Docker image is built using the 'docker build' command. The '-t' flag is used to specify the name and tag of the Docker image. Command docker build . -t node-todo-app:latest

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/369bcc18-a304-4e6f-af33-599693c17bae">

To check the images, use the command "docker images".

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/332191a6-387c-40cb-ba5e-a8d29bc71418">




