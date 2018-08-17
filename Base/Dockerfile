# This dockerfile is used to the sparkcluster for YunFangData. 
# VERSION 1 - EDITION 1
# Author: GSY (Honglin Huang)
# Command format: Instruction [arguments / command] ..

# Operation System: Centos7
FROM centos:7
MAINTAINER GSY <coder.gsy@gmail.com>


# Install System Manage Tools
RUN yum update -y
RUN yum upgrade -y
RUN yum install -y ssh curl man unzip nano wget gcc

RUN yum -y install java-1.8.0-openjdk
RUN yum -y install epel-release mysql-devel python-devel
RUN yum -y install python-pip && yum clean all
 
ENV JAVA_HOME /usr/lib/jvm/jre-1.8.0-openjdk/

# Spark Configure
COPY spark-2.2.1-bin-hadoop2.7.tgz /

WORKDIR spark

RUN tar -zxvf /spark-2.2.1-bin-hadoop2.7.tgz
RUN mv /spark/spark-2.2.1-bin-hadoop2.7/* ./

RUN rm -rf /spark/spark-2.2.1-bin-hadoop2.7.tgz /spark/spark-2.2.1-bin-hadoop2.7
 
ENV SPARK_HOME /spark
ENV PATH /spark/bin:$PATH
ENV PATH /spark/sbin:$PATH

RUN mv $SPARK_HOME/conf/spark-defaults.conf.template $SPARK_HOME/conf/spark-default.conf
RUN echo "spark.sql.execution.arrow.enabled true" >> $SPARK_HOME/conf/spark-default.conf
