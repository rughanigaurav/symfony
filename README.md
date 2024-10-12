#### Steps to Build and Run Docker in Windows System (You must have Docker-Desktop Installed in System)

1.  Clone the repository
    git clone https://github.com/rughanigaurav/symfony.git

2.  After cloned go to project directory

3.  run the below commands in terminal to build docker

    docker-compose up --build

4.  after execution please verify all the docker-images using docker-compose ps

5.  your symfony project will accessible on http://localhost:8080

6.  your phpmyadmin will be accessible on http://localhost:8081

7.  Symfony project directory should src/public/ and Python project directory should be app/

# Steps to install Install Docker and Docker Composer in Ubuntu

# Getting started with Docker

# install docker in ubuntu

```bash
sudo apt-get update

sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin

sudo docker run hello-world
```

# install docker-compose in ubuntu

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version
```

# Remove sudo from Docker

```bash
sudo groupadd docker

sudo usermod -aG docker $USER

newgrp docker

docker run hello-world
```

> **_'You successfully Installed the Docker!'_**

## CLone the Repository

```bash
$ git clone https://github.com/rughanigaurav/symfony.git
```

## Build the Docker

### run the Command in the project folder(where docker-compose.yml exist) from terminal :

```bash
$ docker-compose build
```

### run the Docker

```bash
$ docker-compose up
```

#### Notes

1.  your symfony project will accessible on http://localhost:8080

2.  your phpmyadmin will be accessible on http://localhost:8081

3.  Symfony project directory should src/public/ and Python project directory should be app/
