FROM r-base:4.3.1

RUN apt-get update && apt-get install -y curl libcurl4-openssl-dev libxml2-dev procps

RUN cd /opt && curl -LJO https://raw.githubusercontent.com/davidebolo1993/VISOR/43895dccc9f475a1dcbc5e75b75856f367cc6200/scripts/randomregion.r

RUN cd /opt && Rscript randomregion.r --help

RUN cd /opt && printf '#!/usr/bin/env bash\nRscript /opt/randomregion.r "$@"\n' > randomregion.sh

RUN cd /opt && chmod 775 randomregion.sh

RUN ln -s /opt/randomregion.sh /usr/local/bin/randomregion

RUN apt-get remove curl -y

# randomregion.r script packaged with VISOR

# Recipe: https://github.com/GallVp/docker-images

# Invoked as `randomregion --help`