FROM python:3

WORKDIR /usr/src/app

COPY . .
RUN mkdir /logs

# upgrade pip
RUN pip install --upgrade pip

# install dependancy
RUN pip install -r requirements.txt

