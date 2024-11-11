# Use Ubuntu as base image
FROM python:3.6-slim-buster

# Set environment variables
ENV DEBIAN_FRONTEND noninteractive

# Update and install necessary packages
# RUN apt-get update && \
#     apt-get install -y \
#     python3.6 \
#     python3-pip \
#     git
RUN apt update -y
RUN apt-get install git -y
RUN apt-get install libglib2.0-0 -y
RUN apt install -y libsm6 libxext6
RUN apt-get install libxrender1 -y

RUN mkdir sketch-image

ADD sketch-image/ /sketch-image
ADD keras-contrib /keras-contrib



RUN ls

# Change working directory

WORKDIR /sketch-image


# Install Python dependencies

RUN pip3 install -r requirements.txt
RUN pip3 install git+https://www.github.com/keras-team/keras-contrib.git

# RUN python3 ../keras-contrib/setup.py install

# Define default command to run when the container starts
CMD jupyter notebook --no-browser --ip 0.0.0.0 --port 8888 --allow-root
