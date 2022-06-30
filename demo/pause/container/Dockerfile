FROM ubuntu@sha256:8da4e9509bfe5e09df6502e7a8e93c63e4d0d9dbaa9f92d7d767f96d6c20a78a

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y build-essential curl

COPY pause.c /
RUN gcc pause.c -o /pause

CMD curl https://demo.avolens.net/pause && /pause
