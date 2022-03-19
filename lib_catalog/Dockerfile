FROM python:3.6-alpine
WORKDIR /app
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
COPY . .
RUN \
 apk add --no-cache postgresql-libs g++ bash gcc libxslt-dev && \
 apk add --no-cache --virtual .build-deps musl-dev postgresql-dev && \
 pip install --upgrade pip && \
 python -m pip install -r requirements.txt --no-cache-dir && \
 apk --purge del .build-deps
EXPOSE 8000
CMD python manage.py runserver 0.0.0.0:8000