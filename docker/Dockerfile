FROM alpine:3.21
LABEL maintainer="i@cuile.com"
# setup smartdns and webproc
ENV WEBPROC_VERSION=0.4.0
ENV WEBPROC_URL=https://github.com/jpillora/webproc/releases/download/v${WEBPROC_VERSION}/webproc_${WEBPROC_VERSION}_linux_amd64.gz

ENV SMART_VERSION=Release46
ENV SMARTDNS_URL=https://github.com/pymumu/smartdns/releases/download/${SMART_VERSION}/smartdns-x86_64

RUN curl -L ${WEBPROC_URL} | gzip -d - > /usr/sbin/webproc \
    && chmod +x /usr/sbin/webproc \
    && curl -Lo /usr/sbin/smartdns ${SMARTDNS_URL} \
    && chmod +x /usr/sbin/smartdns
COPY ../conf/smartdns.conf /etc/smartdns.conf
EXPOSE 53/udp
# run
ENTRYPOINT ["webproc","-c","/etc/smartdns.conf","smartdns","-f","-x","-c","/etc/smartdns.conf"]