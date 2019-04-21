## How to run

- Make sure you have downloaded latest `docker` running in your OS

- Clone this project and follow the steps mentioned below

- Build the app running the command, which creates a Docker image, which we’re going to name using the `--tag` option. Use `-t`
  if you want to use the shorter option.
  ```
  $ docker build --tag=hello-html .
  ```
- Run the app, mapping your machine’s port `4000` to the container’s published port 80 using `-p`
  ```
  $ docker run -p 4000:80 hello-html
  ```

- On Windows, explicitly stop the container;
  On Windows systems, `CTRL+C` does not stop the container. So, first type CTRL+C to get the prompt back (or open another shell),
  list all the running containers,
  ```
  $ docker container ls
  ```
  Stop the running container using,
  ```
  $ docker container stop <Container NAME or ID>  to stop the container.
  ```
  Otherwise, you get an error response from the daemon when you try to re-run the container in the next step.

- Run the app in the `background`, in detached mode
  ```
  $ docker run -d -p 4000:80 hello-html
  ```
  You get the `long container ID` for your app and then are kicked back to your terminal. Your container is running in the `background`.
