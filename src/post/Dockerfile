FROM python:3.6.0-alpine

WORKDIR /app
ADD . /app

RUN apk add --no-cache build-base gcc musl-dev
RUN pip install -r /app/requirements.txt
RUN chmod 644 post_app.py

ENV POST_DATABASE_HOST post_db
ENV POST_DATABASE posts

ENTRYPOINT ["python3", "post_app.py"]
