
## Docker Demo


### Build App

``` docker build -t demo .```

### Run the App

```docker run -p 4000:80 demo```

http://localhost:4000/


### Find IP address of Docker Machine

```docker-machine ip .```

### Share your image

- Login with your docker id

```docker login```

- Tag the image

```docker tag demo adarshdch/get-started:demo```

- Publish the image

```docker push adarshdch/get-started:demo```

- Pull the image

```docker pull adarshdch/get-started:demo```

- Pull and run the image from the remote repository

```docker run -p 4000:80 adarshdch/get-started:demo```

Reference:

https://docs.docker.com/get-started/part2/