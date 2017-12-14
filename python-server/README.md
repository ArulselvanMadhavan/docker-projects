# Docker Build Exercise Day 1

Your challenge is to create your first Dockerfile that is a static web server.

- Create a Dockerfile that runs a Python 3 static web server from Ubuntu using the command `python -m http.server 8000`.
- There should be a `www` directory that contains the contents of the static site. Just a single `index.html` file will do.
- The contents of the `www` directory should be copied into `/usr/src/app` which also should be the working directory for the image.
- Create a Makefile that has:
  - One command for building the Docker image.
  - One command for running the image.
  - One command for running the image in dev mode where it volume mounts the `www` directory to `/usr/src/app`.
