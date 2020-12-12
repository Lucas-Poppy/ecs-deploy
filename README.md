## 起動
docker-compose up -d

## 停止
docker-compose down

## ECR PUSH

aws ecr get-login-password --region ap-northeast-1 | docker login --username AWS --password-stdin **********.dkr.ecr.ap-northeast-1.amazonaws.com

docker build -t ecs-deploy/nuxt -f ./docker/nuxt/prod/Dockerfile .
docker tag ecs-deploy/nuxt:latest **********.dkr.ecr.ap-northeast-1.amazonaws.com/ecs-deploy/nuxt:latest
docker push **********.dkr.ecr.ap-northeast-1.amazonaws.com/ecs-deploy/nuxt:latest

docker build -t ecs-deploy/express -f ./docker/express/prod/Dockerfile .
docker tag ecs-deploy/express:latest **********.dkr.ecr.ap-northeast-1.amazonaws.com/ecs-deploy/express:latest
docker push **********.dkr.ecr.ap-northeast-1.amazonaws.com/ecs-deploy/express:latest