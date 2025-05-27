FROM python:3.12

RUN apt-get update && \
    apt-get install -y \
    git \
    wkhtmltopdf \
    curl \
    libcurl4 \
    procps

RUN pip install --upgrade pip

RUN pip install markdown==3.7 \
    matplotlib \
    numpy \
    pdfkit \
    pysam \
    scipy

RUN cd /usr/src && \
    git clone https://github.com/gallvp/hic_qc.git && \
    cd /usr/src/hic_qc && \
    git checkout v1.3 && \
    pip install -e . -vvv

ENV PATH="${PATH}:/usr/src/hic_qc"

RUN if [ -d "/usr/lib/x86_64-linux-gnu/" ]; then strip --remove-section=.note.ABI-tag /usr/lib/x86_64-linux-gnu/libQt5Core.so.5; fi

# A (very) simple script to QC Hi-C data.

# From: [https://github.com/gallvp/hic_qc](https://github.com/gallvp/hic_qc)

# Version 1.3 forked from upstream 1.2 https://github.com/phasegenomics/hic_qc
