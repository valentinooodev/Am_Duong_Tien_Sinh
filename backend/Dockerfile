FROM python:3.10.8-slim-buster
ENV PYTHONWRITEBYTECODE=1
ENV PYTHONBUFFERED=1
WORKDIR /backend
RUN apt update && apt install -y libpq-dev gcc
COPY requirements.txt /backend
RUN pip install --upgrade pip && pip install -r requirements.txt
RUN pip install psycopg2
COPY . /backend