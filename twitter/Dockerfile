FROM phusion/baseimage

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update -qq && \
    apt-get install -y -q --no-install-recommends \
    python2.7 python-pip build-essential python-dev

RUN pip install --upgrade pip
RUN pip install -U setuptools
RUN pip install Flask requests
# application source code including static files, templates, etc
ADD src /app/src

ENTRYPOINT ["python", "-u", "/app/src/app.py"]
