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


