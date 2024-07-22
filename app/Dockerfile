# Use the official Python runtime as a parent image
FROM python:3.10-slim

# Set the working directory inside the container
WORKDIR /code

# Copy the requirements file into the container at /code
COPY ./app/requirements.txt .

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir --upgrade -r ./requirements.txt

# Copy the entire source directory into the container at /code
COPY ./app/src ./src

# Expose the port that the application runs on
EXPOSE 8000

# Define the command to run your FastAPI application when the container starts
CMD ["fastapi", "run", "./src/main.py", "--host", "0.0.0.0", "--port", "8000", "--reload"]
