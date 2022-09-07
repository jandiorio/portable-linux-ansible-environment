FROM python:slim-buster

WORKDIR /working

COPY . .

RUN apt update && apt -y install git gcc sshpass sudo

RUN pip install -r requirements.txt

EXPOSE 22

ENTRYPOINT [ "/bin/bash" ]
