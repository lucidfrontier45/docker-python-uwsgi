FROM python:3.4
MAINTAINER Shiqiao Du <lucidfrontier.45@gmail.com>

RUN set -ex \
	&& buildDeps=' \
		libc6-dev \
		libpcre3-dev \
		mime-support \
	' \
	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* \
	&& pip install --no-cache-dir uwsgi
