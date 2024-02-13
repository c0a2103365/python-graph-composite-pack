FROM julia

USER root

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y sudo


COPY ./gpu.jl /gpu.jl

RUN cd / && \
    julia ./gpu.jl

RUN sudo apt install -y build-essential

WORKDIR /