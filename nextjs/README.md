# NEXT JS

Development setup for Next JS

The Dockerfile pulls the latest version of Node. Along with it, we are exposing PORT 3000 (can be changed) and setting up an Entry point for the container.

To build this image, execute the following command:

```
docker build -t {image-name} .
```

Once the image is created (and this image can be reused as well for other projects), we need to run the Docker compose run command

```
docker-compose run --rm -p 3000:3000 {service_name}
```
