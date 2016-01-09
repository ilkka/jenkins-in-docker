# Need to match the base image with jenkins, which is debian-based
FROM debian:jessie
MAINTAINER Ilkka Laukkanen <ilkka@ilkka.io>

# We deffo know jenkins has uid 1000 in the jenkins-master image
RUN useradd -d "/var/jenkins_home" -u 1000 -m -s /bin/bash jenkins

RUN mkdir -p /var/log/jenkins \
  && chown -R jenkins:jenkins /var/log/jenkins

VOLUME ["/var/log/jenkins", "/var/jenkins_home"]

USER jenkins

CMD ["echo", "Jenkins Data container"]
