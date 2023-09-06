FROM debian:bullseye-slim

RUN apt-get update && apt-get install -y git make gcc procps

RUN cd /opt && git clone https://github.com/GallVp/fasta_validator.git
RUN cd /opt/fasta_validator && git checkout a6a2ec1901ea973932b6e6ad3bfeaaab4df48a8d
RUN cd /opt/fasta_validator && make
RUN cd /opt/fasta_validator && make install
RUN cd /opt && rm -r fasta_validator

# - fasta_validator from https://github.com/GallVp/fasta_validator.git which is a fork of https://github.com/linsalrob/fasta_validator

# - Change in the forked version: Allowed stop codon in the end of a sequence

# - Recipe: https://github.com/GallVp/docker-images

# - Invoked as `fasta_validate -v fasta_file.fasta`

# - The a6a2ec1_ps version also includes the `procps` package to allow collection of task metrics