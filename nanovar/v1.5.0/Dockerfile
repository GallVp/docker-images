FROM debian:bullseye

RUN apt-get update
RUN apt-get install -y git procps python3 python3-pip
RUN apt-get install -y bedtools samtools minimap2
RUn apt-get clean

RUN git clone https://github.com/cytham/nanovar
RUN cd nanovar && git checkout 08d2c8b351d4d9fdf3a5970cdad9148de9fd44d9
RUN cd nanovar && pip3 install numpy==1.19.5 tensorflow-cpu==2.5.0 scipy biopython pybedtools matplotlib natsort progress pysam htmlark cytocad
RUN cd nanovar && python3 setup.py install

# nanovar

# Recipe: https://github.com/GallVp/docker-images

# Invoked as `nanovar --help`