from r-base:4.3.2

RUN apt-get update
RUN apt-get install -y pandoc procps cmake texlive-latex-base lmodern texlive-latex-recommended

RUN R -e "install.packages('rmarkdown',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('lemon',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('tinytex',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('ggsci',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('dplyr',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('reshape2',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('forcats',repos='http://cran.us.r-project.org')"
RUN R -e "install.packages('rsq',repos='http://cran.us.r-project.org')"