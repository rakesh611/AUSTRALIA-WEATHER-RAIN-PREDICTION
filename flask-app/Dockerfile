# Dockerfile inside flask-app/
FROM python:3.9-slim
WORKDIR /app

# Copy app code
COPY . /app/

# Copy model from relative path (adjust path if needed)
COPY ../CODE/artifacts/models/model.pkl /app/CODE/artifacts/models/model.pkl

RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 5000
CMD ["python", "application.py"]
