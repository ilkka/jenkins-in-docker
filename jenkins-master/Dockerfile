# Totally based off of http://engineering.riotgames.com/news/docker-jenkins-data-persists

FROM jenkins:1.625.3
MAINTAINER Ilkka Laukkanen <ilkka@ilkka.io>

USER root
RUN mkdir -p /var/log/jenkins /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins /var/cache/jenkins
USER jenkins

ENV JAVA_OPTS="-Xmx2048m" \
  JENKINS_OPTS="--handlerCountStartup=10 --handlerCountMax=30 --logfile=/var/log/jenkins/jenkins.log --webroot=/var/cache/jenkins/war"
