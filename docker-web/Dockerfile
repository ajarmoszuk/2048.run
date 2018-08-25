FROM ubuntu:18.04

COPY gotty gotty
COPY 2048 /usr/local/bin/2048
COPY wrapper.sh wrapper.sh

RUN chmod +x gotty
RUN chmod +x /usr/local/bin/2048
RUN chmod +x wrapper.sh

EXPOSE 8080

CMD ["./wrapper.sh"]
