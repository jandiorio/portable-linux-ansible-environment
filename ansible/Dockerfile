FROM python:slim-buster

WORKDIR /working

COPY . .

RUN apt update && apt -y install git gcc sshpass sudo openssh-server openssh-client

RUN useradd -ms /bin/bash autoadmin
RUN echo "autoadmin:admin" | chpasswd
RUN usermod -aG sudo autoadmin
RUN service ssh start

RUN pip install -r requirements.txt

EXPOSE 22
ENTRYPOINT service ssh restart && bash
# ENTRYPOINT [ "/bin/bash" ]
