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

Step 5: Create a docker container Create a Docker container A Docker container is created using the Docker image that was built in the previous step. The '-d' flag is used to run the container in detached mode, and the '-p' flag is used to map port 8000 of the container to port 8000 of the host machine.

Commands docker run -d -p8000:8000 node-todo-app:latest

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/aee09ba8-2db6-4ad6-936c-4d04b95435a6">

The user can check the running containers by using the command "sudo docker ps".

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/e3b3fefd-01b8-4d33-b3a4-646311295a8d">

Step 6: Open port 8000 in the instance’s security inbound rule Open port 8000 in the instance’s security inbound rule To allow traffic to access the application, port 8000 needs to be opened in the instance’s security inbound rule.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/d80bebc3-f014-4970-a215-da482ab63c40">

Step 7: Check if the application is running Check if the application is running Finally, we can check if the application is running by opening a browser and typing the URL 'http://<host_ip_address>:8000' in a web browser.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/44c9cd55-1ee9-42be-8f48-be74ccb385cc">

**Project on Building and Deploying a Node.js Application with Docker on Ubuntu using Jenkins CI/CD Pipeline **

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/395d891e-4c88-489b-950f-aaf695b9ff97">

The project aims to set up a Jenkins cluster consisting of a master node, an agent node, and a live server using three AWS EC2 instances. The project requires installing Java, Jenkins, and Docker on the master and agent nodes. The Jenkins cluster distributes the workload across multiple nodes, and the master node controls and assigns jobs to agent nodes. A pipeline is created to deploy a Node.js application using Docker. The pipeline has stages such as checkout, build, test, push, and deploy, which perform different tasks such as fetching source code from GitHub, building a Docker image, testing the image, pushing it to DockerHub, and deploying it to the live server. The project helps in automating the deployment process and saves time and effort by eliminating manual tasks.

Pre-Requisites:

1.3 EC2 Instance (1 for Jenkins Master-Node, 1 for Jenkins Agent-Node and 1 for Deploying live sever)

2.Jenkins and Java Installation in Master-Node Only Java Installation in Agent-Node

3.Docker Installation

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/4909aa29-80a0-45d5-860c-9cffc139a826">

Step 1: Set up a Jenkins Cluster (Master Node and Agent Node) • Jenkins can be configured as a single server or as a cluster of servers, where the workload is distributed across multiple nodes. • In a Jenkins cluster, multiple Jenkins instances, called nodes, work together to execute jobs. Each node has its own resources (such as CPU, memory, and disk space) and can perform builds independently. • The Jenkins master controls the cluster and assigns jobs to the agent nodes based on their availability and workload. • When a job is submitted to the Jenkins master, it decides which node to run the job on, based on the configured load balancing algorithm. The job is then executed on the selected node.

Jenkins is an open-source automation server that provides a platform for continuous integration and continuous delivery (CI/CD). It is widely used in software development to automate the build, test, and deployment processes. Jenkins can be configured as a single server or as a cluster of servers, where the workload is distributed across multiple nodes.

The benefits of using a Jenkins cluster are as follows

1. Scalability: A Jenkins cluster can scale horizontally by adding more agent nodes to distribute build and deployment tasks. This allows the cluster to handle larger workloads without overloading the master node.

2. High availability: With a Jenkins cluster, if one node fails, the cluster can still continue to function as other nodes can pick up the workload. This ensures high availability of the Jenkins services.

3. Improved performance: By distributing build and deployment tasks across multiple nodes, a Jenkins cluster can improve performance and reduce the time it takes to complete tasks.

4. Resource utilization: A Jenkins cluster can utilize resources more efficiently by distributing the workload across multiple nodes. This can help reduce the idle time of resources and increase their utilization.

5. Flexibility: A Jenkins cluster can be easily customized to meet the specific needs of a development team. Nodes can be added or removed based on workload, and different types of nodes can be used for different types of tasks.

Prerequisite:

1. Two AWS EC2 Instance

1-instance for Master-Node and another 1-instance for Agent-Node with Ubuntu OS

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/bfdae626-0bf1-404d-a62c-3e0fcaa19a0e">

2. Java installation in both EC2 instances

3. Jenkins installation in EC2 instance of Master-Node

(Use this website to install Jenkins and Java for Linux OS )

https://www.jenkins.io/doc/book/installing/linux/

Step 1: Creating ssh key pair in Master Node.
· Follow the commands to generate the ssh-keygen

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/f5186f86-332a-4d69-866c-7f1a09ceedcd">

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/8227f1e3-cea1-476d-a513-51621c4e410a">

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/e805c61c-38ff-4264-afaf-27ccf3df58f6">

Step 2: Connecting Agent Node to Master Node
· Copy the public key (id_rsa.pub) which was generated in the master node

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/ac62d08f-a45e-45d4-bff4-a553eaca556d">

· Past the public key in Agent Node of the .ssh directory of the authorized_keys file.

Commands to follow

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/f89f16ef-35eb-4e6e-8a9b-6c0359c89dee">

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/e66ab92a-c2eb-4d74-bba8-f44f6f9adb97">

Step 3: Cross-checking the Master-Node is connected to Agent-node
· Open the master-node terminal and run the following command to get access to the agent node in the master-node terminal.

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/57e652ee-8c82-43ad-ab50-8752c40c36a7">

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/89f8396e-2a6a-42aa-87ce-58486c64e6b6">
<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/db379c65-8b22-4b9a-b917-48c3ab31e15f">

Successfully connected to agent node in the master-node terminal.

Step 4: Setting Agent in Jenkins-Master-Node.
· Open Jenkins-Master server

<img width="587" alt="image" src="https://github.com/pradeepyedam/Project-on-Building-and-Deploying-a-Node.js-Application-with-Docker-on-Ubuntu/assets/134625420/e9f3a477-7248-4728-9cc6-b82a1d8458ec">

· Click on Set up an agent

· Give a name to Node and select Agent type as a permanent agent

· Give a Description and give a number of executors as 1.

· In the Remote root directory, give the working path of agent-node as /home/ubuntu

· Give a label and in usage select “Use this node as much as possible”.

· In the launch method, select “launch agents via SSH”.

· In HOST, Put public_ip of Agent-node



















