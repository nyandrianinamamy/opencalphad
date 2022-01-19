FROM amd64/debian:bullseye-slim as base

FROM base as builder-base
RUN apt-get update \
    && apt-get install gfortran build-essential -y
WORKDIR /usr/local/bin
COPY . /usr/local/bin/.
RUN make

FROM builder-base as development
WORKDIR /app