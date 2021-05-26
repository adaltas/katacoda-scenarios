
## Step 5 - Build and run it again

1. Rebuild the image:

  `docker build -t webserver .`

2. Run it using different port and container name:

  `docker run -d -p 8090:80 --name www1 webserver`

3. Verify the updated output with `curl`:

  `curl localhost:8090`
