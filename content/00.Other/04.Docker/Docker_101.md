## Docker Installation and Usage Guide

**Introduction**

Docker is an open-source platform for developing, shipping, and running applications. It enables developers to package their applications and their dependencies into a lightweight, portable, and self-sufficient container image. This makes it easier to deploy and manage applications on any infrastructure, from local development machines to production servers.

![](https://www.lucidchart.com/publicSegments/view/55523fca-f854-4078-a110-33310a00ce79/image.png)

**Installation**

**Prerequisites**

* A Linux or macOS operating system
* A recent version of Docker installed

**Steps**

1. Update your system packages:

```
sudo apt update && sudo apt upgrade -y
```

2. Install the following packages:

```
sudo apt install apt-transport-https ca-certificates curl gnupg2 software-properties-common -y
```

3. Add the Docker GPG key:

```
sudo curl -LR https://download.docker.com/linux/debian/gpg -o /etc/apt/trusted.gpg.d/docker.gpg.asc
```

4. Add the Docker repository to your system:

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"
```

5. Update your system packages again:

```
sudo apt update
```

6. Install Docker:

```
sudo apt install docker-ce -y
```

**Usage**

**Basic Commands**

* `docker run` - Run a container
* `docker images` - List images
* `docker ps` - List containers
* `docker stop` - Stop a container
* `docker rm` - Remove a container

**Pulling Images**

To run a container, you first need to pull an image from Docker Hub. An image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries, and settings.

To pull an image, use the `docker pull` command:

```
docker pull nginx
```

This will download the latest version of the nginx image from Docker Hub and store it on your local machine.

**Running Containers**

To run a container, use the `docker run` command:

```
docker run nginx
```

This will start a new container based on the nginx image and run it in the foreground. The container will exit once the application inside it has finished running.

**Stopping and Removing Containers**

To stop a container, use the `docker stop` command:

```
docker stop <container_id>
```

To remove a container, use the `docker rm` command:

```
docker rm <container_id>
```

**Further Learning**

* Docker Documentation: [https://docs.docker.com/](https://docs.docker.com/)
* Docker Tutorials: [https://docs.docker.com/get-started/](https://docs.docker.com/get-started/)
* Docker Examples: [https://docs.docker.com/samples/](https://docs.docker.com/samples/)

## Docker Compose

**Introduction**

Docker Compose is a tool for defining and running multi-container applications. With Docker Compose, you can define the services that make up your application, as well as their dependencies, in a single YAML file. Docker Compose will then take care of starting and stopping the containers, as well as linking them together.

**Installation**

**Prerequisites**

* Docker installed

**Steps**

1. Download the Docker Compose binary:

```
curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```

2. Make the binary executable:

```
sudo chmod +x /usr/local/bin/docker-compose
```

3. Test the installation:

```
docker-compose --version
```

**Usage**

To use Docker Compose, you first need to create a YAML file that defines your application. This file is called a `docker-compose.yml` file.

The following is an example of a `docker-compose.yml` file for a simple web application:

```
version: '3'

services:
  web:
    image: nginx:latest
    ports:
      - "80:80"

  app:
    image: my-app:latest
    depends_on:
      - web
```

This file defines two services: a web service and an app service. The web service is based on the nginx image, and it listens on port 80. The app service is based on the `my-app` image, and it depends on the web service being started first.

To start the application, run the following command:

```
docker-compose up
```

