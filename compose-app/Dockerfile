# syntax=docker/dockerfile:1
FROM docker.io/python:slim

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

WORKDIR /app

ARG UID=10001
RUN adduser \
    --disabled-password \
    --gecos "" \
    --home "/nonexistent" \
    --shell "/sbin/nologin" \
    --no-create-home \
    --uid "${UID}" \
    appuser

COPY requirements.txt .
RUN python -m pip install -r requirements.txt

USER appuser

COPY . .

EXPOSE 8080
CMD python app.py
