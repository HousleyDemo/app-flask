FROM registry.access.redhat.com/ubi9/python-39:1-117.1684741281

# Install any needed packages specified in requirements.txt
COPY docker/requirements.txt /

RUN pip install -r /requirements.txt


# Set the working directory in the container
WORKDIR /code/project


# Copy the content of the local src directory to the working directory
COPY project /code/project



EXPOSE 8081/tcp
ENV FLASK_PORT=8081
CMD [ "python", "./app.py" ]

