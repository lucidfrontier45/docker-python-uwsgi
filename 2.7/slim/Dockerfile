FROM python:2.7-slim
MAINTAINER Shiqiao Du <lucidfrontier.45@gmail.com>

RUN set -ex \
	&& buildDeps=' \
		gcc \
		libbz2-dev \
		libc6-dev \
		libpcre3-dev \
		libssl-dev \
		make \
		zlib1g-dev \
	' \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends $buildDeps \
	&& rm -rf /var/lib/apt/lists/* \
	&& pip install --no-cache-dir uwsgi \
	&& apt-get purge -y --auto-remove $buildDeps

COPY mime.types /etc/mime.types
