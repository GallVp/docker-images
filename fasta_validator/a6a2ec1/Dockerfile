FROM debian:bullseye-slim

RUN apt-get update && apt-get install -y git make gcc

RUN cd /opt && git clone https://github.com/GallVp/fasta_validator.git
RUN cd /opt/fasta_validator && git checkout a6a2ec1901ea973932b6e6ad3bfeaaab4df48a8d
RUN cd /opt/fasta_validator && make
RUN cd /opt/fasta_validator && make install
RUN cd /opt && rm -r fasta_validator
