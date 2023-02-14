FROM jenkins/jenkins:lts
USER root
RUN apt-get update
RUN apt install -y nano curl git
RUN apt-get update && apt-get install -y docker.io
RUN usermod -aG docker jenkins
RUN curl -L https://github.com/docker/compose/releases/download/1.21.2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
RUN chmod +x /usr/local/bin/docker-compose
# RUN chown jenkins:jenkins /var/run/docker.sock
USER jenkins
