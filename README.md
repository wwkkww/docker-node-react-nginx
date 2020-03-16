This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## For Dev environment

## Build image with docker-compose (run Webapp and Test with hot reloading)

```docker-compose up --build```

## Alternative (run test manually with hot reloading)
1. remove tests service from docker-compose yml
2. run ```docker-compose up --build```
3. get container id from ```docker ps```
4. run  ```docker exec -it <container_id> npm run test```

## For Production build using NGINX server

## 1. Build docker image

```docker build .```

## 2. Run docker

```docker run -p <your_localhost_port>:80 <image_id>```

#### Deploy fails with Aws::S3::Errors::SignatureDoesNotMatch
- replace ```secure: $AWS_SECRET_KEY``` with ```secret_acces_key: $AWS_SECRET_KEY```
- https://travis-ci.community/t/deploy-fails-with-aws-signaturedoesnotmatch/5835