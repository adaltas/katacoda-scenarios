
1. Create a home page of a web application. We need to create the `index.html` file in the `./html` directory with the following content:

  ```
  <!DOCTYPE html>
  <html>
    <head>
      <title>This is a title</title>
    </head>
    <body>
      <p>Hello world!</p>
    </body>
  </html>
  ```

2. Enhance our existing `Dockerfile` with the following content:

  ```
  FROM debian
  WORKDIR /var/www/html
  COPY index.html .
  RUN apt-get update && apt-get install apache2 -y && apt-get clean
  CMD ["apache2ctl", "-DFOREGROUND"]
  ```
  
  - The `WORKDIR` instruction sets the working directory for any `RUN`, `CMD`, `ENTRYPOINT`, `COPY` and `ADD` instructions that follow it in the Dockerfile.
  - The `COPY` instruction copies files or directories from the host to the filesystem of the container at the specific path.
  
3. Verify:

  - the `Dockerfile`: `cat Dockerfile`
  - the HTML file: `cat html/index.html`
