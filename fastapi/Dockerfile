# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the current directory contents into the container at /usr/src/app
COPY ./peptide_digest_api.py /usr/src/app
COPY ./requirements_api.txt /usr/src/app

# Install any needed packages specified in requirements_api.txt
RUN pip install --no-cache-dir -r requirements_api.txt

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Run app.py when the container launches
CMD ["uvicorn", "peptide_digest_api:app", "--host", "0.0.0.0", "--port", "8000"]
