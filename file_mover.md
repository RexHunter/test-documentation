==================
File mover(golang)
==================

```
FROM debian:stretch

ENV GOLANG_ARCHIVE=go1.11.4.linux-amd64.tar.gz

RUN apt-get update
RUN apt-get install -y wget maven git

RUN wget ${GOLANG_URL}${GOLANG_ARCHIVE}
RUN tar -C /usr/local -xzf ${GOLANG_ARCHIVE}

ENV PATH $PATH:/usr/local/go/bin

CMD ['/bin/bash']
```
