FROM kalilinux/kali-rolling:latest

ENV DEBIAN_FRONTEND noninteractive

RUN apt update
RUN apt upgrade -y

# Installerer mange basic kali-tools
RUN apt -y install kali-linux-headless

# installerer alle APT packages fra packages.txt
COPY packages.txt packages
RUN apt install $(cat packages) -y


# Installerer Peda og adder til gdb
RUN git clone https://github.com/longld/peda.git ~/peda
RUN echo "source ~/peda/peda.py" >> ~/.gdbinit


# Installerer PWN tools
RUN apt-get -y install python3 python3-pip python3-dev git libssl-dev libffi-dev build-essential
RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install --upgrade pwntools

# Legger til predefinerte alias ol. til bashrc
COPY .bashrc bashrc
RUN cat bashrc >> /root/.bashrc


# working directory satt til home/root
WORKDIR /home/root
