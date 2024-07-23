#base image
FROM python:3.8-slim-buster
# upgrade pip
RUN pip install --upgrade pip 

# Copiying all the files to source directory
COPY . /src

# Set working directory to previously added source directory
WORKDIR /src

# Giving permissions to python file
RUN chmod +x train.py

# Install required python dependencies from requirements file
RUN pip install -r requirements.txt

# Run train.py file
ENTRYPOINT ["python"]

CMD ["train.py"]