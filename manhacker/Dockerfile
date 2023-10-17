FROM kalilinux/kali-rolling:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt update
RUN apt upgrade -y

RUN apt -y install kali-linux-headless

COPY packages.txt packages
RUN apt install $(cat packages) -y

COPY .bashrc bashrc
RUN cat bashrc >> /root/.bashrc
