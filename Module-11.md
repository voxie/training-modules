# Module 11: Docker

## Introduction
Docker containers are an integral part of the development and management of our DevOps workflow. After this module, you should be comfortable with most tasks required to interact and manage containers along with an understanding of their purpose and basic workings.

For this module, *create a new Git repo* for your Docker work in Module 11.

It is recommended that you read through each of the official documentation resources listed below and follow some of the links within each resource to help clarify specific tools and their purposes.

Resources and articles:
- [What is Docker?](https://www.docker.com/what-docker)
- [Official Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)
- [Official Docker Engine Docs](https://docs.docker.com/engine/understanding-docker/)
- [Official Docker Compose Docs](https://docs.docker.com/compose/overview/)
- [Official Docker Hub Docs](https://docs.docker.com/docker-hub/overview/)

---

## The Test

_Throughout these steps, there are instructions to paste information into a file called docker-module.txt. For each instruction that you are asked to paste output, provide the task number as a prefix to the output._

1. Install [Docker Toolbox](https://docs.docker.com/mac/step_one/) on your local machine. Don't forget to run `/usr/local/bin/docker-machine env default` and `eval $(/usr/local/bin/docker-machine env default)` use the default environment.
2. Create a [Docker Hub](https://hub.docker.com/) account.
3. Login to your Docker Hub account using `docker login` in your terminal window.
4. Pull down the `alpine:3.3` image from Docker Hub.
5. Create a new file called _docker-module.txt_ and paste the output of `docker images` into the file.
6. Run `sh` interactively inside of the `alpine:3.3` container using `docker run`. You should see a prompt showing `/ #`.
7. Using `apk`, install bash while inside of the container. You'll need add bash using the `--no-cache` flag.
8. Start a bash prompt inside of the container and paste the current prompt into _docker-module.txt_.
9. Exit the container.
10. Attempt to run `bash` inside of the container. Paste the output into _docker-module.txt_.
11. Create a new _Dockerfile_ that extends the `alpine:3.3` and installs `bash`.
12. Build a new image with the tag `realpage/alpine-bash:3.3` using your new _Dockerfile_.
13. Attempt to run bash inside of the new `realpage/alpine-bash:3.3` container. Paste the output into _docker-module.txt_.
14. Exit the container.
15. Create a new executable file called _welcome.sh_ containing the following:
```
#!/bin/bash
echo 'Hello, World!'
```
16. Update the _Dockerfile_ to `COPY` the _welcome.sh_ file to `/home/welcome.sh`.
17. Rebuild the container following the the changes.
18. Run the _welcome.sh_ script within the container using `docker run`, and paste the output into _docker-module.txt_.
19. Update the _Dockerfile_ to run the _welecome.sh_ script via the `CMD` instruction.
20. Rebuild the container and run it via `docker run realpage/alpine-bash:3.3`.
21. Paste the output into _docker-module.txt_.

---

## Wrapping Up

When you are done, verify you have pushed your changes to GitHub. Please create a tag called v1.0 with a message of "ready for review" in your docker repo. Be sure your tags are pushed to the remote repository and are visible in GitHub.

Create an issue titled *Review Module 11 - Docker* and @mention your mentor and team leader.
