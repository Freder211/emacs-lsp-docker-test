FROM python:latest

RUN addgroup --gid 1000 user && \
    adduser --disabled-password --gecos '' --uid 1000 --gid 1000 user


RUN mkdir /app && chown user:user /app
WORKDIR /app

USER user
ENV PATH="${PATH}:/home/user/.local/bin/"

COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

RUN pip install pyright
