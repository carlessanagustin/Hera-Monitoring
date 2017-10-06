FROM ubuntu:16.04

ENV GRAPHITE_VERSION=1.0.2
ENV PYTHONPATH="/opt/graphite/lib/:/opt/graphite/webapp/"

RUN apt-get update && \
    apt-get -y install python-dev libcairo2-dev libffi-dev build-essential python-pip && \
    pip install --upgrade pip && \
    pip install whisper==$GRAPHITE_VERSION && \
    pip install carbon==$GRAPHITE_VERSION && \
    pip install graphite-web==$GRAPHITE_VERSION

#		pip install --no-binary=:all: https://github.com/graphite-project/whisper/tarball/master && \
#		pip install --no-binary=:all: https://github.com/graphite-project/carbon/tarball/master && \
#		pip install --no-binary=:all: https://github.com/graphite-project/graphite-web/tarball/master
