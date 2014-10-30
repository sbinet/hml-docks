##
## higgsml/hml-base container holds data and code for all HiggsML containers
##
FROM golang

MAINTAINER binet@cern.ch

RUN mkdir -p \
    /higgsml/data \
    /higgsml/run \
    /higgsml/code

RUN apt-get install -y curl
RUN curl -L http://cern.ch/binet/higgsml/test.csv >     /higgsml/data/test.csv \
 && curl -L http://cern.ch/binet/higgsml/training.csv > /higgsml/data/training.csv

RUN go get -v -u github.com/sbinet/hml/...

