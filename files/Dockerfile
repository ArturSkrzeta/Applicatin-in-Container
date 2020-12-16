# set base image from docker hub
FROM python:3.8

# set the working directory in the container
WORKDIR /code

# copy the dependencies file to the working directory
COPY requirements.txt .

# install dependencies
RUN pip install -r requirements.txt

COPY closed.csv .
COPY created.csv .
COPY Weekly_IT_KPI.csv .

# copy the content of the local src directory to the working directory
COPY kpi.py .

# command to run on container start
CMD [ "python", "./main.py" ]
