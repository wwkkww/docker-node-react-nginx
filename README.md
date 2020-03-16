This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## For Dev environment

## Build image with docker-compose (run Webapp and Test with hot reloading)

```docker-compose up --build```

## Alternative (run test manually with hot reloading)
1. remove tests service from docker-compose yml
2. run ```docker-compose up --build```
3. get container id from ```docker ps```
4. run  ```docker exec -it <container_id> npm run test```

## Use NGINX server for production build

## 1. Build docker image

```docker build .```

## 2. Run docker

```docker run -p <your_localhost_port>:80 <image_id>```