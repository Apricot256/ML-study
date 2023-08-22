FROM ubuntu:22.04

# set timezone
ENV TZ=Asia/Tokyo
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# update and install essential packages
RUN apt-get update -y
RUN apt install -y python3.10 python3-pip git libgl1-mesa-dev libglib2.0-0

# Latex
# RUN apt install -y evince texlive-fonts-extra texlive-fonts-recommended texlive-lang-cjk xdvik-ja

# install python packages
COPY ../.devcontainer/requirements.txt /tmp
RUN pip3 install -r /tmp/requirements.txt