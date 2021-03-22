# DockerizingMERNStack

## Install Docker

$ sudo apt update

// over https prerequisites

$ sudo apt install apt-transport-https ca-certificates curl software-properties-common

// Then add the GPG key for the official Docker repository to your system:

$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

//  Add the Docker repository to APT sources:

$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"

// Next, update the package database with the Docker packages from the newly added repo:

$ sudo apt update

// Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:

$ apt-cache policy docker-ce

// Finally, install Docker:

$ sudo apt install docker-ce

// Check docker status

$ sudo systemctl status docker

## Building Docker out of MERN stack app

// get Dockerfile that says Dockerfile for React client
// and place it in client folder

// then run frontend with this command

$ docker build -t react-app .

// To verify everything is fine, we run our newly built container using the command:

$ docker run -p 3000:3000 react-app

// get Dockerfile that says Dockerfile for Node Express Backend
// and place it in server folder

// We can simply build our Backend with this command:

$ docker build -t node-app .

// We need multidocker component for docker-compose

// In the main directory of the project, (outside the server/client) get a file named docker-compose.yml

// To create the build for the entire application, we need to run the following command: (use sudo if error)

$ docker-compose build

// We can start the multi-container system using the following simple command:

$ docker-compose up

// We can inspect running services using the docker-compose ps command.


