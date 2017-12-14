ARG UBUNTU_VERSION=18.04
FROM ubuntu:${UBUNTU_VERSION}

ARG WWW_ROOT=/usr/src/app

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install python3.6 -y && \
    rm -rf /var/lib/apt/lists/*

WORKDIR ${WWW_ROOT}

COPY www ${WWW_ROOT}

EXPOSE 8080

CMD ["python3.6", "-m", "http.server", "8080"]

