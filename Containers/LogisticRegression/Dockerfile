FROM debian:11-slim

WORKDIR /app

RUN apt-get update && apt-get -y dist-upgrade

RUN apt-get -y install apt-utils \
    build-essential \
    python3 \
    gcc \
    python3-dev \
    python3-pip \
    python3-numpy \
    python3-pandas
    
ADD requirements.txt .
RUN pip3 install -r requirements.txt
ENV FLASK_ENV=development
COPY logisticRegression.py /app/logisticRegression.py
ENTRYPOINT [ "python3", "./logisticRegression.py"]
