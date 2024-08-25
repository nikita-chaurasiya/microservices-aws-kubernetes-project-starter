FROM python:3.8-slim-bullseye

WORKDIR /src

COPY ./analytics/requirements.txt requirements.txt

COPY . .

RUN apt update -y 

RUN apt install build-essential libpq-dev -y

RUN pip install --upgrade pip setuptools wheel

RUN pip install -r requirements.txt

COPY ./analytics/app.py app.py

COPY ./analytics/config.py config.py

CMD ["python3", "./app.py"]

