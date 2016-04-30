FROM python:3.5
MAINTAINER Shiqiao Du <lucidfrontier.45@gmail.com>

RUN set -ex \
	&& buildDeps=' \
		libc6-dev \
		libpcre3-dev \
	' \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends $buildDeps \
	&& apt-get install -y mime-support \
	&& rm -rf /var/lib/apt/lists/* \
	&& pip install --no-cache-dir uwsgi
