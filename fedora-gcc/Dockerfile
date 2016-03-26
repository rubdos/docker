FROM fedora:rawhide

RUN dnf groupinstall -y "C Development Tools and Libraries"
RUN dnf install -y git cmake

RUN dnf install -y python3-pip
RUN pip3 install coala-bears

RUN dnf clean all
