# TL;DR

Please make sure you have a Docker Hub account, and bring your laptop fully charged with Docker set-up.
See below for some further instructions and details. 

# Create a Docker Hub account (hub.docker.com)

You will need a Docker Hub account to access the course materials

# Setup Docker on your laptop

Please make sure to bring your laptop (fully charged if possible :) ).

## Linux users

you need you to install Docker engine and Docker compose. Make sure you have Docker compose version 1.6 or higher by running docker-compose version from the command prompt. 

## Mac users

You need to install Docker for Mac or if you have an older Mac, Docker Toolbox. 

## Windows users

Attention : le plus important des prerequis est l'espace disponible sur le Docker Host (votre ordinateur ou VM de travail). Pour pouvoir faire tous les labs Windows Container il faudra pull les 2 Base Images de Microsoft :
* Windows Server Core (microsoft/windowsservercore) qui fait 8Go
* Nano Server (microsoft/nanoserver) qui fait 800Mo

Les explications sur pourquoi cette taille vous seront données durant la presentation :)

Il vous faudra donc 10Go d'espace disponible (qui seront liberés apres les Labs)

### Windows 7 / 8 / 8.1 / 10 **avant** Anniversary Update

il vous faudra installer une VM Windows Server 2016 en evaluation ou bien Windows 10 pro 1607 (AE (Anniversary Update (du mois d'aout 2016)))

Puis installer dans la VM [Docker for Windows](https://docs.docker.com/docker-for-windows/) en version beta (la stable n'a pas pour l'instant le switch entre container Linux et Windows d'integré dans le clic droit sur l'icone dans le systray)

### **A partir de** Windows 10 Anniversary Update (du mois d'aout 2016) (version 1607 Pro ou Entreprise)

il vous faudra être à jour sur Windows Update, l'AE RTM est la version 14393.0, il faut être au moins en build 14393.222 (la version actuelle au 11/11/16 est 14393.447)

> Pour verifier la version de votre Windows 10 lancer `winver.exe`

Installer ensuite [Docker for Windows](https://docs.docker.com/docker-for-windows/) en version beta (la stable n'a pas pour l'instant le switch entre container Linux et Windows d'integré dans le clic droit sur l'icone dans le systray)

Note : Il ne faut pas mixer les hyperviseurs sur le Docker Host, si VirtualBox ou VMware Workstation est installé il faudra les desinstaller. Durant le process d'installation Hyper-V est activé et doit être le seul hyperviseur sur l'ordinateur.

> Pour plus de details voir [setup steps in the Windows Container lab](https://github.com/docker/labs/blob/master/windows/windows-containers/Setup.md)

#### ! Attention !

[Docker Toolbox](https://docker.github.io/toolbox/) ne permet que le support des containers Linux pas Windows

### Ensuite recuperer les Base Images Microsoft

Lancer PowerShell

```
docker pull microsoft/windowsservercore
docker pull microsoft/nanoserver
```

# New to Docker ?

pre-pull the docker images for the very basic tutorial so you’re ready for the beginner level course.

```
docker pull hello-world 
docker pull alpine 
docker pull seqvence/static-site
```

# Already know Docker (at least a little bit) ?

To run the application and participate in the rest of the training, pre-pull these images

```
docker pull microsoft/dotnet:1.0.0-preview1 
docker pull node:5.11.0-slim 
docker pull python:2.7-alpine 
docker pull redis:alpine
docker pull postgres:9.4
```

# Ops / orchestration part

Please pre-build the demo app by running the following steps

```
git clone git://github.com/jpetazzo/orchestration-workshop
cd orchestration-workshop/dockercoins
docker-compose build
```

# Select your courses

Think about which course you’d like to complete during the event. Don’t worry if you’re not sure which course to complete. Mentors will be there to help you pick which course is right for you!

## Dev Beginner - Linux

This tutorial will guide you through the steps involved in setting up your computer, running your first containers, deploying a web applications with Docker and running a multi-container voting app with Docker Compose. 

## Dev Beginner - Windows

This tutorial will walk you through setting up your environment, running basic containers and creating a Docker Compose multi-container application using Windows containers.

## Dev Intermediate

This tutorial teaches you how to network your containers, how you can manage data inside and between your containers and how to use Docker Cloud to build your image from source and use comme developer tools and programming languages with Docker. 

## Ops Beginner

The beginner part of the Ops tutorial will teach you how to set up a swarm, how to use it to host your own registry, how to build your app container images and how to deploy and scale a distributed application called Dockercoins. 

## Ops Intermediate

From global container scheduling, overlay networks troubleshooting, dealing with stateful services and node management, this tutorial will show you how to operate your swarm cluster at scale and take you on a swarm mode deep dive. 

# Questions / Let us know

Have any questions or concerns? Join the conversation on the global-mentor-week slack channel on our Docker Community slack team. Sign up to the Docker Community here to be invited to the slack team. We really hope to see you at the event! Please spread the word by clicking to tweet and encouraging friends / colleagues to RSVP and #LearnDocker. 

See you on Tuesday @Epitech
The Mentor team
