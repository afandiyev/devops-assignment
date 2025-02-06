FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt /app

RUN pip install --no-cache-dir -r requirements.txt

COPY . /app

RUN useradd -m appuser && chown -R appuser /app
USER appuser

EXPOSE 5000

ENTRYPOINT ["python"]
CMD ["app.py"]
