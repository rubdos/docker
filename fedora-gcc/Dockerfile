FROM fedora:rawhide

RUN dnf groupinstall -y "C Development Tools and Libraries"
RUN dnf install -y git cmake npm
RUN dnf install -y zlib-devel libpng-devel OpenEXR-libs OpenEXR-devel \
        ilmbase-devel freetype-devel libxml2-devel libjpeg-devel \
        libtiff-devel python3-devel extra-cmake-modules

RUN dnf install -y python3-pip
RUN npm install -g remark
RUN pip3 install coala-bears

RUN dnf clean all
