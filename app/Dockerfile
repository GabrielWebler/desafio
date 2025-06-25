
FROM python:3.7.4-slim-buster

WORKDIR /app

#COPY requirements.txt .
COPY * .

RUN pip install --no-cache-dir -r requirements.txt

#COPY api.py .

EXPOSE 8000

CMD ["gunicorn", "--log-level", "debug", "-b", "0.0.0.0:8000", "api:app"]