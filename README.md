# Breaking down monoliths 🪨⛏️

This problem statement has two objectives:
- Get familiar with reading error stack trace and debugging code.
- Convert a monolith architecture based docker-compose application into a microservices based architecture.  

## Requirements:
- [docker](https://docs.docker.com/engine/) and [docker-compose](https://docs.docker.com/compose/install/). Follow the guides based on your operating system.
- Internet. Pull docker image `python:3.8-alpine` beforehand to avoid connectivity issues.

## Initial directory structure
```
├── README.md
├── docs
│   └── <documentation related images/files>
├── microservices
│   ├── Docker-compose.yaml
│   ├── landing
│   │   ├── app
│   │   │   ├── app.py
│   │   │   ├── requirements.txt
│   │   │   └── templates
│   │   │       └── index.html
│   │   └── Dockerfile
│   │
```
## Monolith architecture diagram
<p align="center">
  <img src="docs/microservices-initial.drawio.png" />
</p>

## Build & Run
```
# under the microservices directory
# NOTE: For any code changes to be reflected, the build command must be rerun, and then up
docker-compose build
# run without the -d flag incase you want to observe the logs
docker-compose up -d
```
### To stop the services in detached mode
```
docker-compose down
```

**NOTE**: It is possible your first build will not be successful and that's alright. Read the stack trace and debug the errors. The resources and links provided within the manual are sufficient to successfully complete the project.

## Microservices-based architecture diagram
<p align="center">
  <img src="docs/microservices-final.drawio.png" />
  
<h7 align="center">The diagram only shows the services already defined within the microservice architecture for visualization purposes. You still need to add services of your own.</h7>

</p>




