FROM debian:bullseye

RUN apt-get update && apt-get install -y git python3 python3-pip wkhtmltopdf curl libcurl4 procps

RUN cd /usr/bin && ln -s ./python3 ./python

RUN cd /usr/src && git clone https://github.com/phasegenomics/hic_qc.git

RUN cd /usr/src/hic_qc && git checkout 6881c3390fd4afb85009a52918b4d068100c58b4

RUN cd /usr/src/hic_qc && cat requirements.txt | sed 's|==.*||g' | xargs pip install

ENV PATH="${PATH}:/usr/src/hic_qc"

RUN if [ -d "/usr/lib/x86_64-linux-gnu/" ]; then strip --remove-section=.note.ABI-tag /usr/lib/x86_64-linux-gnu/libQt5Core.so.5; fi

# A (very) simple script to QC Hi-C data.

# From: [https://github.com/phasegenomics/hic_qc](https://github.com/phasegenomics/hic_qc)

# The 6881c33_ps version also includes the `procps` package to allow collection of task metrics.