FROM python:3.5-slim-buster
ENV PYTHONUNBUFFERED=1
ENV SECRET_KEY supersecretkey
RUN apt-get -y update && apt-get -y upgrade

#psycopg2 dependencies

RUN apt-get -y install postgresql-contrib
RUN apt-get -y install libpq-dev gcc
RUN apt-get -y install python3-dev
RUN apt-get -y install libpq5 libc6

#pillow dependencies
RUN apt-get -y install libjpeg62-turbo-dev zlib1g-dev libtiff-dev libfreetype6 libfreetype6-dev libwebp-dev libopenjp2-7-dev libopenjp2-7-dev -y

RUN apt-get -y install libgraphviz-dev

WORKDIR /backend
COPY ./requirements.txt /backend/
EXPOSE 8000
RUN pip install -r requirements.txt
COPY . /backend/
