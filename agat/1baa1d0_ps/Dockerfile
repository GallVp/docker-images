FROM ubuntu:noble

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get -y install libdb-dev
RUN apt-get -y install libbio-perl-perl libclone-perl libgraph-perl liblwp-useragent-determined-perl libstatistics-r-perl libcarp-clan-perl libsort-naturally-perl libfile-share-perl libfile-sharedir-install-perl libyaml-perl liblwp-protocol-https-perl libfile-sharedir-perl libmoose-perl libterm-progressbar-perl libdevel-cover-perl
RUN apt-get -y install git

RUN cd /opt && git clone https://github.com/NBISweden/AGAT.git
RUN cd /opt/AGAT && git checkout 1baa1d0d44d44dc2365a5ce9e0c01ad528643523
RUN cd /opt/AGAT && perl Makefile.PL
RUN cd /opt/AGAT && make install

# - AGAT:       https://github.com/NBISweden/AGAT.git
# - Version:    1baa1d0d44d44dc2365a5ce9e0c01ad528643523
# - Recipe:     https://github.com/GallVp/docker-images
