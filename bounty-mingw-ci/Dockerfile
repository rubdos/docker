FROM rubdos/fedora-mingw

RUN git clone https://github.com/TheBounty/Core.git

RUN cd Core && mkdir build && cd build && \
        mingw64-cmake \
        -DWITH_QT=off \
        -DWITH_YAF_PY_BINDINGS=off .. && \
        make -j4
