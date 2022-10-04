FROM python:3.8.5

WORKDIR /app

COPY requirements.txt . 

RUN pip install -r --no-cache-dir ./requirements.txt 

COPY . .

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]