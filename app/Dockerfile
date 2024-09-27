# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set environment variables for Python
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container
COPY . /app

# Copy the requirements.txt file into the container
COPY requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose port 5000 for Flask app
EXPOSE 5000

# Set the entry point for the application
CMD ["python", "app.py"]

# Run the Flask app with auto-reload using Flask’s development server
CMD ["flask", "run", "--host=127.0.0.1", "--port=5000"]
