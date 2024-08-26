# Use the latest Ubuntu base image
FROM ubuntu:latest

# Update the APT package list and upgrade all packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED error if it appears
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Copy the Flask app code into the container
COPY api.py /app/api.py

# Set the working directory
WORKDIR /app

# Expose the port the Flask app will run on
EXPOSE 5252

# Command to run the Flask app
CMD ["python3", "api.py"]
