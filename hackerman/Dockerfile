FROM almalinux:latest

RUN dnf group install 'Development Tools' -y

COPY packages.txt packages

RUN dnf install $(cat packages) -y
