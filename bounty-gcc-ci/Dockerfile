FROM rubdos/fedora-gcc

RUN dnf install -y zlib-devel libpng-devel OpenEXR-libs OpenEXR-devel \
        ilmbase-devel freetype-devel libxml2-devel libjpeg-devel libtiff-devel\
        python3-devel

RUN git clone https://github.com/TheBounty/Core.git

RUN cd Core && mkdir build && cd build && \
        cmake -DWITH_QT=off -DWITH_YAF_PY_BINDINGS=off .. && make -j4

ENV BOUNTY_PATH /Core
