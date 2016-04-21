FROM python:3.5-slim
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
	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* \
    && pip install --no-cache-dir uwsgi \
    && apt-get purge -y --auto-remove $buildDeps
