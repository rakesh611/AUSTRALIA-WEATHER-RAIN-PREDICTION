# Use Python 3.9 slim as base
FROM python:3.9-slim

WORKDIR /app

# Copy flask app code
COPY flask-app/ /app/

# Copy the model file
COPY CODE/artifacts/models/model.pkl /app/CODE/artifacts/models/model.pkl

# Create a clean requirements file
RUN echo "Flask\npandas\nnumpy\nscikit-learn\nsetuptools\nmatplotlib\nseaborn\njoblib\nxgboost" > requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose Flask port
EXPOSE 5000

# Start the app
CMD ["python", "application.py"]
