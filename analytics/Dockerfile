FROM python:3.8-slim-bullseye

WORKDIR /src

COPY requirements.txt requirements.txt

COPY . .

RUN apt update -y && apt install build-essential libpq-dev -y

RUN pip install --upgrade pip setuptools wheel

RUN pip install -r requirements.txt

CMD ["python3", "./app.py"]
