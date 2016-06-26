FROM python:2.7
MAINTAINER Shiqiao Du <lucidfrontier.45@gmail.com>

RUN set -ex \
	&& buildDeps=' \
		libc6-dev \
		libpcre3-dev \
	' \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends $buildDeps \
	&& rm -rf /var/lib/apt/lists/* \
	&& pip install --no-cache-dir uwsgi

COPY mime.types /etc/mime.types
