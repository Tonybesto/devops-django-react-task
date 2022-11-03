## find a way to install libpq-dev and python3-dev on the machines
# FROM python:3.10.8-alpine3.16
FROM ubuntu:20.04

RUN mkdir /backend

COPY . /backend/

WORKDIR /backend

RUN apt update -y 

RUN apt install -y python3-pip

RUN apt install libpq-dev python3-dev -y

RUN pip install -r requirements.txt

RUN python3 manage.py migrate

RUN python3 manage.py runserver

EXPOSE 8000

CMD ["python3", "manage.py" , "runserver"]