FROM alpine:3.20

RUN apk update \
        && apk --no-cache add dnsmasq

COPY dnsmasq.conf /etc/dnsmasq.conf

ENTRYPOINT ["dnsmasq", "--no-daemon"]
