FROM 192.168.6.207:5000/spark-kafka-base

MAINTAINER GSY <coder.gsy@gmail.com>

COPY master.sh /

ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG /spark/logs

EXPOSE 8080 7077 6066

CMD ["/bin/bash","/master.sh"]
