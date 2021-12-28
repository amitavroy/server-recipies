# Laravel development image

Development setup for Laravel 8x

The Dockerfile pulls the latest version of PHP along with composer. Along with it, we are exposing PORT 80 (can be changed) and setting up an Entry point for the container.

To start development, copy this folder into the root of the Laravel installation, change the name of the container and run the following command:

```
docker-compose up
```
