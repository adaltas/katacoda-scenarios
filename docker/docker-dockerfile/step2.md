
## Step 2 - Build an image

1. We can build a Docker image by executing `docker build -t webserver .`

  The docker build command builds an image from the `Dockerfile` and a context. The `PATH` is a directory on your local filesystem (currently is `.`).

  The Docker daemon runs the instructions in the `Dockerfile` one-by-one, committing the result of each instruction to a new image if necessary, before finally outputting the ID of your new image.

2. View the image on your host:

  - `docker images`
  - `docker history webserver`
