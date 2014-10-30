##
## higgsml/xgboost holds the xgboost code
##
FROM higgsml/hml-base
MAINTAINER binet@cern.ch

RUN apt-get update -y
RUN apt-get install -y git make gcc g++ python python-numpy python-scipy

ENV BUILD_DIR /higgsml/code

RUN mkdir -p $BUILD_DIR && \
    git clone git://github.com/hetong007/higgsml $BUILD_DIR
RUN chmod +x $BUILD_DIR/higgsml-*
RUN cd $BUILD_DIR && ./higgsml-build

## run the training
RUN cd $BUILD_DIR && \
    ./higgsml-train /higgsml/data/training.csv /higgsml/code/trained.dat

## for convenience
RUN cd $BUILD_DIR && \
    ln -s /higgsml/data/training.csv . && \
    ln -s /higgsml/data/test.csv     .

WORKDIR /higgsml/data

ENTRYPOINT /bin/bash
