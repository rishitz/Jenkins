FROM ubuntu:latest

#Install Openssh 
RUN apt update && apt install openssh-sever sudo -y

#Create the User and change its password

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 jenkins
RUN echo 'jenkins:jenkins' | chpasswd
RUN service ssh start


#Expose SSh Port of container
 EXPOSE 22
 
WORKDIR /home/ubuntu/
