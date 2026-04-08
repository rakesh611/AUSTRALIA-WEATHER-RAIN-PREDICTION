# Dockerfile at repo root
FROM python:3.9-slim

WORKDIR /app

# Copy Flask app
COPY flask-app/ /app/

# Copy model file
COPY CODE/artifacts/models/model.pkl /app/CODE/artifacts/models/model.pkl

# Install dependencies
RUN pip install --no-cache-dir -r flask-app/requirements.txt

# Expose Flask port
EXPOSE 5000

# Run Flask app
CMD ["python", "application.py"]
