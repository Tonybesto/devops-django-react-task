## find a way to install libpq-dev and python3-dev on the machines
FROM python:3.8.3-alpine

ENV DockerHOME=/home/app/webapp

RUN mkdir -p $DockerHOME

WORKDIR $DockerHOME

ENV PYTHONDONTWRITEBYTECODE 1

ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip

COPY . $DockerHOME         

RUN pip install -r requirements.txt

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]

#FROM ubuntu:20.04

#RUN mkdir /backend

#COPY . /backend/

#WORKDIR /backend

#RUN apt update -y 

#RUN apt install -y python3-pip

#RUN apt install libpq-dev python3-dev -y

#RUN pip install -r requirements.txt

#RUN python3 manage.py migrate

#RUN python3 manage.py runserver

#EXPOSE 8000

#CMD ["python3", "manage.py", "runserver"]