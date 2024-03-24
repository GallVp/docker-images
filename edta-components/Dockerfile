FROM mambaorg/micromamba:1.5.7

RUN micromamba install -y -n base -c conda-forge -c bioconda \
    bioconda::trf \
    bioconda::mdust \
    bioconda::tesorter \
    conda-forge::procps-ng && \
    micromamba clean --all --
