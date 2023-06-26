# docker-2048
This repository contains a Dockerfile that builds an image for an Nginx web server with the popular 2048 game.

## Prerequisites
Docker installed on your system.

## Usage
1. Clone this repository:
`git clone https://github.com/nolliechyTW/docker-2048.git`
2. Navigate to the project directory:
`cd docker-2048`
3. Build the Docker image:
`docker build -t nginx-2048 .`
4. Run a Docker container based on the created image:
`docker run -p 80:80 nginx-2048`
5. Open your web browser and visit http://localhost to access the 2048 game.

## Customization
If you want to use a different Nginx configuration file or modify any other settings, you can update the `nginx.conf` file and rebuild the Docker image.

## Note
The 2048 game is developed and maintained by [Gabriele Cirulli](https://github.com/gabrielecirulli/2048). For more information about the game, please refer to the official repository.

## Demo
![2048 - Google Chrome 2023-06-27 00-21-40](https://github.com/nolliechyTW/docker-2048/assets/106467497/9c09f067-aa71-4063-814d-c60730da8529)
