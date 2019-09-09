# Traffy_API_Demo
Demo for testing Object Detection API via Docker container

## Requirement
Docker Compose 1.6.0+ and require a Docker Engine of version 1.10.0+.
Reference: https://docs.docker.com/compose/compose-file/compose-versioning/

## Request API

### start docker compose
```
cd <PATH to DIR>/docker-compose
docker-compose up -d
```

### making request
```
from Docker-compose
curl -F "image=@road/<image file> http://localhost:5000/"
```

## Illustration
```
cd "$(pwd)/docker-compose"
docker-compose up -d
from Docker-compose
curl -F "image=@road/pit22.jpg" http://localhost:5000/"
```
### Result
![json response from RESTful API](https://github.com/S-Nuttapong/Traffy_API_Demo/issues/2#issue-490867812)

compare to detection result from inference(python script):

![output image from inference](/docker-compose/Test_Result/pit22.jpg)
