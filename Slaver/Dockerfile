FROM 192.168.6.207:5000/spark-kafka-base

MAINTAINER GSY <coder.gsy@gmail.com>
COPY slaver.sh /

ENV SPARK_WORKER_WEBUI_PORT 8081
ENV SPARK_WORKER_LOG /spark/logs
ENV SPARK_MASTER "spark://10.30.1.9:50002"

EXPOSE 8081

CMD ["/bin/bash","/slaver.sh"]

