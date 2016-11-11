TLDR: RSVP, make sure you have a Docker Hub account, and bring your laptop fully charged with Docker set-up. See below for some further instructions and details. 

1. Create a Docker Hub account here: You will need a Docker Hub account to access the course materials. 

2. Set-up Docker on your laptop (you will need to bring your own computer) 

Linux users: we need you to install Docker engine and Docker compose. Make sure you have Docker compose version 1.6 or higher by running docker-compose version from the command prompt. 
Mac users: install Docker for Mac or if you have an older Mac, Docker Toolbox. 
Windows users: if you have Windows 10 pro install Docker for Windows, otherwise install Docker Toolbox. If you want to try the new Windows containers, go through the setup steps in the Windows Container lab. It is essential to run this command in Powershell before coming to the event:

    docker pull microsoft/windowsservercore:latest

3. New to Docker? pre-pull the docker images for the very basic tutorial so you’re ready for the beginner level course.

    docker pull hello-world 
    docker pull alpine 
    docker pull seqvence/static-site

4. To run the application and participate in the rest of the training, pre-pull these images

    docker pull microsoft/dotnet:1.0.0-preview1 
    docker pull node:5.11.0-slim 
    docker pull python:2.7-alpine 
    docker pull redis:alpine
    docker pull postgres:9.4

5. For the Ops / orchestration part, you will want to pre-build the demo app by running the following steps

    git clone git://github.com/jpetazzo/orchestration-workshop
    cd orchestration-workshop/dockercoins
    docker-compose build

Think about which course you’d like to complete during the event. Don’t worry if you’re not sure which course to complete. Mentors will be there to help you pick which course is right for you!

Dev Beginner - Linux: This tutorial will guide you through the steps involved in setting up your computer, running your first containers, deploying a web applications with Docker and running a multi-container voting app with Docker Compose. 

Dev Beginner - Windows: This tutorial will walk you through setting up your environment, running basic containers and creating a Docker Compose multi-container application using Windows containers.

Dev Intermediate: This tutorial teaches you how to network your containers, how you can manage data inside and between your containers and how to use Docker Cloud to build your image from source and use comme developer tools and programming languages with Docker. 

Ops Beginner: The beginner part of the Ops tutorial will teach you how to set up a swarm, how to use it to host your own registry, how to build your app container images and how to deploy and scale a distributed application called Dockercoins. 

Ops Intermediate: From global container scheduling, overlay networks troubleshooting, dealing with stateful services and node management, this tutorial will show you how to operate your swarm cluster at scale and take you on a swarm mode deep dive. 

Have any questions or concerns? Join the conversation on the global-mentor-week slack channel on our Docker Community slack team. Sign up to the Docker Community here to be invited to the slack team. We really hope to see you at the event! Please spread the word by clicking to tweet and encouraging friends / colleagues to RSVP and #LearnDocker. 

See you on Tuesday @Epitech
The Mentor team
