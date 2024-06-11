FROM rocker/binder:4.4.0
LABEL maintainer='mathesong'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}



RUN wget https://github.com/mathesong/OHBM2024_tutorial/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://mran.revolutionanalytics.com/snapshot/2024-06-11/')); devtools::install_deps()"

RUN rm DESCRIPTION.1; exit 0
