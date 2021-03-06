# Traffy_API_Demo
This is on going project from [Traffy Demo](https://github.com/S-Nuttapong/Traffy_Demo)

Testing Object Detection API for Public Sanitation and Infrastructure  with  Docker Container

## Requirement
Docker Compose 1.6.0+ and Docker Engine of version 1.10.0+.
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
curl -F "image=@road/<image file> http://localhost:5000/
```

## Illustration
```
cd "$(pwd)/docker-compose"
docker-compose up -d
from Docker-compose
curl -F "image=@road/pit22.jpg" http://localhost:5000/
```
### Result

Result from RESTful API:

![json response from RESTful API](https://user-images.githubusercontent.com/52415315/64502947-17d17680-d2f3-11e9-8479-339aa996a8eb.png)

compare to detection result from inference(python script):

![output image from inference](/docker-compose/Test_Result/pit22.jpg)
