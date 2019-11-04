FROM jupyter/datascience-notebook:latest
USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get install software-properties-common -y
RUN apt-get install screen -y
USER jovyan
COPY requirements.txt /tmp/
RUN yes w | pip install -r /tmp/requirements.txt
CMD start-notebook.sh