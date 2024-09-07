FROM ubuntu:20.04

# Set working directory
WORKDIR /app

# Copy requirements and application files
COPY requirements.txt /app/
COPY devops /app/

# Update and install dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install -r requirements.txt

# Expose the port on which the application will run
EXPOSE 8000

# Default entrypoint for the container
ENTRYPOINT ["python3", "manage.py"]

# Run the application
CMD ["runserver", "0.0.0.0:8000"]
