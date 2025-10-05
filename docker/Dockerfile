FROM ubuntu:latest

ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=UTC

RUN apt-get update && \
    apt-get install -y \
    inkscape \
    fontconfig \
    fonts-liberation \
    fonts-dejavu-core \
    fonts-freefont-ttf

RUN fc-cache -fv

ARG KTVERSION_FILE="/sbin/ktversion"

RUN echo "#!/usr/bin/env bash" > ${KTVERSION_FILE} && \
    echo -n "echo " >> ${KTVERSION_FILE} && \
    echo -n "Inkscape-$(inkscape --version | awk '{print $2}')-" >> ${KTVERSION_FILE} && \
    chmod +x ${KTVERSION_FILE}

ENTRYPOINT ["/usr/bin/inkscape"]