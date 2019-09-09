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
![json response from RESTful API](<img width="741" alt="Screen Shot 2562-09-09 at 11 08 03" src="https://user-images.githubusercontent.com/52415315/64502947-17d17680-d2f3-11e9-8479-339aa996a8eb.png">)

compare to detection result from inference(python script):

![output image from inference](/docker-compose/Test_Result/pit22.jpg)
