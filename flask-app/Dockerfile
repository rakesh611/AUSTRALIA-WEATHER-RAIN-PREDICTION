# Dockerfile
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Copy Flask app code
COPY flask-app/ /app/

# Create directories for model, templates, static
RUN mkdir -p /app/CODE/artifacts/models \
    && mkdir -p /app/templates \
    && mkdir -p /app/static

# Add model from GitHub
ADD https://raw.githubusercontent.com/rakesh611/AUSTRALIA-WEATHER-RAIN-PREDICTION/main/CODE/artifacts/models/model.pkl /app/CODE/artifacts/models/model.pkl

# Add templates
ADD https://raw.githubusercontent.com/rakesh611/AUSTRALIA-WEATHER-RAIN-PREDICTION/main/CODE/templates/index.html /app/templates/index.html

# Add static files
ADD https://raw.githubusercontent.com/rakesh611/AUSTRALIA-WEATHER-RAIN-PREDICTION/main/CODE/static/style.css /app/static/style.css

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose Flask port
EXPOSE 5000

# Run Flask app
CMD ["python", "application.py"]
