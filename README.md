# Docker Wordpress

If docker, docker-compose not exist, then install at section [Installation Docker](#Installation%Docker)

## Run Wordpress

Clone project docker compose.

```bash
git clone https://github.com/huynhminhtan/docker-wordpress-stater.git
cd docker-wordpress-starter
````

Then build and run.

```bash
docker-compose stop
docker-compose rm -f
docker-compose up --build -d
docker logs <containerid> # logs
```

Then in your browser listen port 8000, edit port it up to you:

```bash
http://localhost:8000/
```

## Installation Docker

```bash
# Docker
$ sudo apt-get update
$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
$ sudo apt-key fingerprint 0EBFCD88
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
$ sudo apt-get update
$ sudo apt-get install docker-ce
$ sudo docker run hello-world
$ sudo docker --version
```

## Installation Docker Compose

```bash
# Docker-compose
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
docker-compose version 1.23.2, build 1110ad01
```
