FROM ubuntu:18.04

RUN useradd -m -d /tmp -s /usr/local/bin/2048 play
RUN echo 'play:play' | chpasswd
RUN apt update -y && apt install xinetd telnetd -y

COPY 2048 /usr/local/bin/2048
COPY 2048-server /2048-server
COPY id_rsa /id_rsa
COPY telnet /etc/xinetd.d/telnet
COPY motd /etc/issue.net

RUN chmod +x /usr/local/bin/2048
RUN chmod +x /2048-server
RUN echo "" > /etc/issue

EXPOSE 23
EXPOSE 22

CMD service xinetd start && ./2048-server
