FROM python:3.10.8-alpine3.16

RUN mkdir /backend

COPY . /backend/

WORKDIR /backend



RUN  chmod +x script.sh && ./script.sh


EXPOSE 8000


CMD ["python", "manage.py", "runserver"]