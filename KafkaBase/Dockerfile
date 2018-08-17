FROM 192.168.6.207:5000/docker-spark-base

MAINTAINER GSY <coder.gsy@gmail.com>

COPY spark-streaming-kafka_2.11-2.2.1.jar /spark/jars
COPY requirements.txt /

RUN pip install -r /requirements.txt
