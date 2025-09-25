FROM ubuntu:25.04

LABEL maintainer="Rojaldo" email="algo@email.com"
LABEL version="1.0"
LABEL description="A Dockerfile for a basic Ubuntu image with Python installed."

# install python and pip
RUN apt update && \
    apt install -y python3 python3-pip && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

COPY ./hola/script.py /app/script.py

WORKDIR /app

# create a user 
RUN useradd -ms /bin/bash appuser
USER appuser
ENTRYPOINT ["python3"]
CMD ["script.py"]
