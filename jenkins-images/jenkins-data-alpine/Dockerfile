FROM alpine:latest
MAINTAINER Calos Liu

RUN addgroup -g 1000 -S jenkins && adduser -S -h "/var/jenins_home" -u 1000 -G jenkins -s /bin/sh jenkins

RUN mkdir -p /var/log/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins

VOLUME ["/var/log/jenkins", "/var/jenkins_home"]

USER jenkins

CMD ["echo", "Data container for Jenkins created"]