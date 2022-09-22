FROM ubuntu:18.04

LABEL maintainer="Calos Liu"

RUN apt -y update
RUN apt -y install curl unzip

VOLUME ["/data/"]

ADD https://releases.hashicorp.com/consul/1.3.0/consul_1.3.0_linux_amd64.zip /tmp/consul.zip
RUN cd /usr/sbin && unzip /tmp/consul.zip && chmod +x /usr/sbin/consul && rm /tmp/consul.zip

COPY consul.json /config/

EXPOSE 53/udp 8300 8301 8301/udp 8302 8302/udp 8400 8500

ENTRYPOINT ["/usr/sbin/consul", "agent", "-config-dir=/config"]

CMD []