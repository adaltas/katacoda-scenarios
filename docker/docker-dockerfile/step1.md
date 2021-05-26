
## Step 1 - Write Dockerfile

1. Create `Dockerfile` with following content in current directory.

  ```
  FROM debian
  RUN apt-get update && apt-get install apache2 -y && apt-get clean
  CMD ["apache2ctl", "-DFOREGROUND"]
  ```
  
  To create and edit a file, you can use Vim (`vi Dockerfile`) or the following syntax:
  
  ```
  cat > Dockerfile << EOF
  <you>
  <content>
  <here>
  EOF
  ```
  
  [Learn Dockerfile instructions](https://docs.docker.com/engine/reference/builder/#format)

2. Verify the file with `cat Dockerfile`

  Above Dockerfile content describes a Debian image with Apache web server installed.

  - `FROM` indicates the base image for our build
  - Each `RUN` line will be executed by Docker during the build
  - Our `RUN` commands must be non-interactive. (You can‘t provide input to Docker during the build.)
  - In many cases, we will add the `-y` flag to `apt-get`.
