# Use Python 3.9 slim image
FROM python:3.9-slim

# Set working directory in container
WORKDIR /app

# Copy requirements first (for better caching)
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application files
COPY flasky/ .

# Expose port 5000
EXPOSE 5000

# Set environment variables
ENV FLASK_APP=hello.py
ENV FLASK_RUN_HOST=0.0.0.0

# Run the application
CMD ["flask", "run"]