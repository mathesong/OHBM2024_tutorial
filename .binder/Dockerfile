
FROM rocker/binder:4.4.0
LABEL maintainer='mathesong'
COPY --chown=${NB_USER} . ${HOME}
USER ${NB_USER}

RUN wget https://github.com/mathesong/OHBM2024_tutorial/raw/master/DESCRIPTION && R -e "options(repos = list(CRAN = 'http://cran.rstudio.com/')); devtools::install_deps()"
RUN R -e "remotes::install_github('mathesong/bloodstream')"
RUN R -e "install.packages('job')"

RUN rm DESCRIPTION.1; exit 0
