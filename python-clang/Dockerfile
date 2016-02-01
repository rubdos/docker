FROM python:3-onbuild

RUN apt-get update && apt-get install -y libclang-dev
RUN echo "/usr/lib/llvm-3.5/lib/" >> /etc/ld.so.conf && ldconfig

