FROM debian:bullseye

RUN apt-get update
RUN apt-get install -y git procps python3 python3-pip
RUN apt-get install -y bedtools r-base samtools minimap2
RUn apt-get clean

RUN git clone https://github.com/gallvp/VISOR.git
RUN cd VISOR && git checkout 215b4ce38445c6b8e559c0b0e1fed14daeacfb3b
RUN cd VISOR && pip3 install -r requirements.txt
RUN cd VISOR && pip3 install --upgrade cython
RUN cd VISOR && pip3 install pyfaidx==0.7.2.2 pysam==0.22.0 pywgsim==0.5.2 pybedtools==0.9.1 mappy==2.26 plotly==5.17.0 numpy==1.26.1
RUN cd VISOR && python3 setup.py install

# VISOR

# Recipe: https://github.com/GallVp/docker-images

# Invoked as `VISOR --help`