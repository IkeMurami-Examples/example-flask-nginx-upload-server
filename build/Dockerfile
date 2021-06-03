FROM ubuntu:latest

LABEL maintainer="petrakov.oleg@yandex.ru"

RUN apt-get update && \
    apt-get install -y python3 && \
    apt-get install -y python3-pip

COPY ../ /app

RUN mkdir -p /tmp/uploads

WORKDIR /app

RUN python3 -m pip install -r requirements.txt
ENTRYPOINT ["python3"]

CMD ["main.py"]