# Collect the Base Image
FROM python:3.11-slim

# Set the Workdir
WORKDIR /app

# Copy requirements.txt first for dependency installation
COPY requirements.txt /app

# Update package lists
RUN apt-get update

# Install necessary packages
RUN apt-get install -y python3 python3-pip

# Install dependencies from requirements.txt
RUN pip install -r requirements.txt

# Copy the devops directory (potentially after dependencies are installed)
COPY devops /app

# Move to devops directory after everything is copied
WORKDIR devops

# Define the main process
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
 
