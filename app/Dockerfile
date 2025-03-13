FROM python:3.9-slim 

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY ./src/myapp.py .

EXPOSE 8888

CMD [ "gunicorn", "--bind", "0.0.0.0:8888", "src.myapp:app"]