
1. Run a `debian` container with `docker run -it debian`

  After pulling image, it will start a container and open Bash into the running container.

2. Install Apache into the running container 

  - run `apt-get update && apt-get install apache2 -y`
  - exit the container when the installation is complete with `exit`

3. Inspect the changes
  
  - List all containers and find the first entry with the image name as `debian`
  - Inspect changes to files and directories on a container's filesystem using `docker diff <CONTAINER>`. This show the list of **added**, **changed** or **deleted** with capital `A`, `C` or `D` respectively prefixed with each file

4. Create an image from changes

  - Create a new image using `docker commit <CONTAINER> <REPOSITORY[:TAG]>`. Associate any name and a tag to the image
  - Run the new image and make sure Apache is already installed with `apache2 -v`
