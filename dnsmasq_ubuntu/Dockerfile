FROM ubuntu:16.04
RUN apt-get update && apt-get install -y dnsmasq \
    && apt-get install -y dnsutils \
    && apt-get install -y less \
    && apt-get install -y emacs-nox
RUN sed  -i -e 's/^#address=\/double-click.net\/127.0.0.1/address=\/dev\/127.0.0.1/' /etc/dnsmasq.conf
EXPOSE 53 53/udp
#EXPOSE 53 53/tcp
#COPY dnsmasq.conf /etc
# CMD service dnsmasq start
# CMD nslookup hoge.dev 127.0.0.1
ENTRYPOINT ["dnsmasq", "-k"]

