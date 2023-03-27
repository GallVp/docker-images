FROM debian:stable

RUN apt-get update && apt-get install -y git python3 python3-pip

RUN cd /usr/bin && ln -s ./python3 ./python

RUN cd /usr/src && git clone https://github.com/phasegenomics/juicebox_scripts.git

RUN cd /usr/src/juicebox_scripts && git checkout a7ae9915401eb677b8058b0118011ce440999bc0

ENV PATH="${PATH}:/usr/src/juicebox_scripts/juicebox_scripts"
