# Module 2: Docker

## Introduction
Docker containers are an integral part of the development and management of our DevOps workflow. After this module, you should be comfortable with basic tasks required to interact and manage containers along with an understanding of their purpose and basic workings.

For this module, *create a new Git repo* for your Docker work in Module 2.

It is recommended that you read through each of the official documentation resources listed below and follow some of the links within each resource to help clarify specific tools and their purposes.

Resources and articles:

- [What is a Container?](https://www.docker.com/resources/what-container)
- [Official Docker Engine Docs](https://docs.docker.com/engine/docker-overview/)
- [Official Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)
- [Official Docker Hub Docs](https://docs.docker.com/docker-hub/)
- [Alpine Linux package management](https://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management)

---

## Completing the Module

1. Install [Docker Community Edition for Mac](https://store.docker.com/editions/community/docker-ce-desktop-mac)
on your local machine.
2. Create a [Docker Hub](https://hub.docker.com/) account if you do not already have one.
  - If you do, please pass that along to a team member so we can add you to our organization.
3. Login to your Docker Hub account using `docker login` in your terminal window.
4. Pull down the `alpine:latest` image from Docker Hub.
5. Create a new file called _docker-module.txt_, and paste the output of `docker images` into the file.
6. Commit your changes and push up.
7. Run `sh` interactively inside of the `alpine:latest` container using `docker run`. You should see a prompt showing `/ #`.
8. Using `apk` ([more info here](http://wiki.alpinelinux.org/wiki/Alpine_Linux_package_management)), install bash while inside of the container. You'll need add bash using the `--no-cache` flag.
9. Start a bash prompt inside of the container, and paste the current prompt into _docker-module.txt_.
10. Exit the container.
11. Commit your changes and push up.
12. Attempt to run `bash` inside of the container, and paste the output into _docker-module.txt_.

    > Since containers are immutable, they start in their original state everytime. Since the original
    state of the container doesn't have `bash` installed, running the container again restarts the container without bash. This is one of the differences between the way containers and virtual
    machines handle state.

13. Commit your changes and push up.
14. Create a new _Dockerfile_ that extends the `alpine:latest` and installs `bash`.
15. Build a new image with the tag `gentux/alpine-bash:{github-username}` using your new _Dockerfile_. e.g. `gentux/alpine-bash:jlaswell`
16. Attempt to run bash inside of the new `gentux/alpine-bash:{github-username}` container, and paste the output into _docker-module.txt_.
17. Exit the container.
18. Commit your changes and push up.
19. Create a new executable file called _welcome.sh_ containing the following:
```
#!/bin/bash
echo 'Hello, World!'
```
20. Update the _Dockerfile_ so that _welcome.sh_ is added to `/home/welcome.sh` when the container is built.
21. Rebuild the container following the the changes.
22. Run the _welcome.sh_ script within the container using `docker run`, and paste the output into _docker-module.txt_.
23. Commit your changes and push up.
24. Update the _Dockerfile_ so that it outputs "Hello, World!" when only running `docker run gentux/alpine-bash:{github-username}`.
25. Rebuild the container and run it via `docker run gentux/alpine-bash:{github-username}`.
26. Paste the output into _docker-module.txt_.
27. Commit your changes and push up.
28. Pull down the `dockercloud/hello-world` image. You can see the _Dockerfile_ for this image [here](https://hub.docker.com/r/dockercloud/hello-world).
29. Run the `dockercloud/hello-world` image without any arguments or flags.

    > The container continues to run and never exits. If you look at the _Dockerfile_, you can see that
    `php-fpm` and `nginx` are running within the container. Since `nginx` is run with `-g "daemon off;"`, the process never exits and neither does the container!
30. Rerun `docker images` and paste the output into _docker-module.txt_.
31. Commit your changes and push up.

---

## Wrapping Up

When you are done, verify you have pushed your changes to GitHub. Please create a tag called v1.0 with a message of "ready for review" in your docker repo. Be sure your tags are pushed to the remote repository and are visible in GitHub.

Create an issue titled **Review Module 2 - Docker** and assign it to [**@generationtux-helmsmen**](https://github.com/generationtux-helmsmen).
