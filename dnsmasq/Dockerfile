FROM alpine:3.4
RUN apk --no-cache add dnsmasq
RUN sed  -i -e 's/^#address=\/double-click.net\/127.0.0.1/address=\/dev\/127.0.0.1/' /etc/dnsmasq.conf
EXPOSE 53 53/udp
# COPY dnsmasq.conf /etc
# CMD dnsmasq
# CMD nslookup hoge.dev 127.0.0.1
ENTRYPOINT ["dnsmasq", "-k",  "--resolv-file=/etc/resolv.conf"]

