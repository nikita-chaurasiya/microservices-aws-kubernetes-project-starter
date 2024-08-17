FROM python:3.10-slim

WORKDIR /app

COPY ./requirements.txt requirements.txt

# Dependencies required for psycopg2 (used for Postgres client)

RUN apt update -y && apt install -y build-essential libpq-dev

RUN pip install --upgrade pip setuptools wheel

# Dependencies are installed during build time in the container itself so we don't have OS mismatch

RUN pip install -r requirements.txt

COPY . .

CMD python app.py
