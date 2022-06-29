FROM ubuntu:22.04
RUN apt update -y
RUN apt install git curl -y
RUN git clone https://github.com/wilczynski87/Take-My-Junk
WORKDIR ./Take-My-Junk
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt install nodejs -y
RUN npm install --save react react-dom react-scripts
RUN node --version
RUN npm --version
RUN apt install iputils-ping -y
#RUN ping -c 2 172.18.0.6
CMD ["npm", "start"]
