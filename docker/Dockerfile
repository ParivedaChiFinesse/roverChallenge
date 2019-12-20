FROM ubuntu:16.04

# General
RUN apt-get update && \
    apt-get install -y python3-pip cmake zlib1g-dev python3-tk python-opencv \
    # Boost libraries
    libboost-all-dev \
    # Scipy requirements
    libblas-dev liblapack-dev libatlas-base-dev gfortran \
    # Pygame requirements
    libsdl-dev libsdl-image1.2-dev libsdl-mixer1.2-dev libsdl-ttf2.0-dev \
    libsmpeg-dev libportmidi-dev libavformat-dev libswscale-dev \
    # Gym
    libav-tools libsdl2-dev swig cmake && \

    apt-get clean autoclean && \
    apt-get autoremove -y
RUN apt-get install -y curl

RUN pip3 install --upgrade pip
RUN pip3 install setuptools && pip3 install pytest && pip3 install pytest-xdist

RUN curl -o /usr/local/bin/patchelf https://s3-us-west-2.amazonaws.com/openai-sci-artifacts/manual-builds/patchelf_0.9_amd64.elf \
    && chmod +x /usr/local/bin/patchelf

RUN pip3 install rl_coach

RUN mkdir -p /home/coach/experiments
WORKDIR /home/coach