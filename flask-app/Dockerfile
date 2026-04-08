# Base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy application code
COPY flask-app/ /app/

# Create necessary directories for model
RUN mkdir -p /app/CODE/artifacts/models

# Download model directly from GitHub
ADD https://raw.githubusercontent.com/rakesh611/AUSTRALIA-WEATHER-RAIN-PREDICTION/main/CODE/artifacts/models/model.pkl /app/CODE/artifacts/models/model.pkl

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose Flask port
EXPOSE 5000

# Set default command
CMD ["python", "application.py"]
