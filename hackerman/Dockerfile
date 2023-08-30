FROM almalinux:latest

# Mange kule tools som man trenger for development
RUN dnf group install 'Development Tools' -y

# Kopierer innholdet fra .bashrc filen i repoet til .bashrc filen i docker containeren
COPY .bashrc bashrc
RUN cat bashrc >> /root/.bashrc

# Henter alle pakkene som ligger i packages.txt og installerer dem på i containeren
COPY packages.txt packages
RUN dnf install $(cat packages) -y
