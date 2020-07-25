FROM ubuntu

LABEL maintainer="hys.kentaro@gmail.com"
LABEL version="1.0"
LABEL description="bcftools"

RUN apt-get update \
	&& apt-get install -y git \
	&& apt-get install -y build-essential \
	&& apt-get install -y zlib1g-dev \
	&& apt-get install -y libbz2-dev \
	&& apt-get install -y liblzma-dev \
	&& apt-get install -y libgsl-dev \
	&& apt-get install -y libcurl4-gnutls-dev \
	&& git clone git://github.com/samtools/htslib.git \
	&& git clone git://github.com/samtools/bcftools.git \
	&& cd bcftools \
	&& make \
	&& make install
