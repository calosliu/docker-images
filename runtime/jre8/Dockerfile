FROM alpine:latest

LABEL maintainer="Calos Liu"

RUN apk update
RUN apk add openjdk8-jre

ENTRYPOINT ["java"]

CMD ["--version"]