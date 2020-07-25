FROM ubuntu

LABEL maintainer="hys.kentaro@gmail.com"
LABEL version="1.0"
LABEL description="bcftools"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
	&& apt-get install -y \
	build-essential \
	zlib1g-dev \
	libbz2-dev \
	liblzma-dev \
	libgsl-dev \
	libcurl4-gnutls-dev \
	git \
	&& git clone git://github.com/samtools/htslib.git \
	&& git clone git://github.com/samtools/bcftools.git \
	&& cd bcftools \
	&& make \
	&& make install
