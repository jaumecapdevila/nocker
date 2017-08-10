# nocker
Basic setup to dockerize an express app

## Prerequisites

First of all you need to have docker and docker-compose installed in your host machine. You can follow the instructions available at the docker's oficial [website](https://docs.docker.com/engine/installation/)

## Setup

By default, once you run the the command `docker-compose up -d` to initialize the environment, all the content (besides the node_modules folder) of the **web** folder will be copied into the working directory `/usr/src/app` specified in the Dockerfile. Feel free to change the source and the destionation folders by modifying the content of the `docker-compose.yml` and the Dockerfile. Finally remember that the node container will run the command `npm install` inside the specified working directory every time the container is started up. In order to add more dependencies into the project just update the content of the `package.json` file and restart the container. 