FROM python:3.7-alpine
 RUN apk add --no-cache --virtual .build-deps \
    gcc \
    python3-dev \
    musl-dev \
    git \
    && apk add --no-cache postgresql-dev \
    && pip3 install --no-cache-dir psycopg2 \
    && git clone https://github.com/SetRandom/gross_buh.git /usr/src/app \
    && apk del .build-deps
ADD "app" /usr/src/app
WORKDIR /usr/src/app
RUN pip install -r ./requirements_docker.txt --no-cache-dir 
CMD ["sh", "run.sh"]