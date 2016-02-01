FROM python:3-onbuild

RUN apt-get update && apt-get install -y libclang-dev
RUN echo "/usr/local/lib/" >> /etc/ld.so.conf && ldconfig

