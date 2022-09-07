FROM python:slim-buster

WORKDIR /workspace

COPY . .

RUN apt update && apt -y install gcc openssh-server openssh-client sudo

RUN useradd -ms /bin/bash ubuntu
RUN echo "ubuntu:ubuntu" | chpasswd
RUN usermod -aG sudo ubuntu
RUN service ssh start

RUN pip install -r requirements.txt

EXPOSE 22

# ENTRYPOINT [ "/bin/bash" ]
ENTRYPOINT service ssh restart && bash
