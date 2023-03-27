FROM debian:stable

RUN apt-get update && apt-get install -y git python3 python3-pip default-jre gawk parallel coreutils

RUN cd /usr/bin && ln -s ./python3 ./python

RUN cd /usr/src && git clone https://github.com/aidenlab/3d-dna.git

RUN cd /usr/src/3d-dna && git checkout 63029aa3bc5ba9bbdad9dd9771ace583cc95e273

RUN pip install scipy numpy matplotlib

RUN echo "exit 0" >> /usr/src/3d-dna/visualize/run-assembly-visualizer.sh

RUN chmod 777 /usr/src/3d-dna/visualize/run-assembly-visualizer.sh

RUN chmod 777 /usr/src/3d-dna/visualize/juicebox_tools.sh

RUN chmod 777 /usr/src/3d-dna/run-3ddna-pipeline.sh