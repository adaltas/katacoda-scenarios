
1. Now we have an image created from `Dockerfile`, we'll run it:

  `docker run -d -p 8080:80 --name www webserver`

2. Verify the output with curl:

  `curl localhost:8080`
