# Offical python image - debian bookworm
FROM python:3.11.6-bookworm

WORKDIR /app

# Install Python services and libaries in requirements.txt
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# now copy the project over
COPY . /app/


# Make port 80 open outside the container
EXPOSE 8000

# Define environment variable
ENV NAME World

# Run /app/main.py when the container launches
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
