# hello-docker

hello-docker is a basic application that outputs "Hello Docker!" to a console. It uses Node + JS.

## Running this app without Docker

- Start with an OS (Windows, Linux, MacOS)
- Install Node (specific version for most cases)
- Copy app files locally (i.e. `git clone`)
- Run `node app.js`

## Running this app with Docker

Package (build) the application:

```bash
> docker build -t hello-docker .
```

Argument breakdown:

- `-t` specifies the tag. In this case, it's `hello-docker`
- `.` specifies the directory where the Dockerfile required to package this application lives.

**Note**: The image won't be stored in this local directory, but don't worry. Docker stores it somewhere else. You can see **every docker image in your machine** by executing `docker image ls` or `docker images` in a CLI.

Example:

```bash
> docker image ls
REPOSITORY    TAG     IMAGE ID   CREATED       SIZE
hello-docker  latest  123456789  1 minute ago  100MB
```

To run the image, the `run` command is needed (`docker run <image-name-goes-here>`):

```bash
> docker run hello-docker
Hello Docker!
```
