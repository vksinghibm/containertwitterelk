FROM phusion/baseimage

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update -qq && \
    apt-get install -y -q --no-install-recommends \
    python2.7 python-pip build-essential python-dev libssl-dev
   
RUN pip install --upgrade pip
RUN pip install -U setuptools
RUN pip install Flask Flask-Cache elasticsearch requests

RUN pip install --upgrade ndg-httpsclient

# application source code including static files, templates, etc
ADD src /app/src

EXPOSE 5000

ENTRYPOINT ["python", "-u", "/app/src/app.py"]
