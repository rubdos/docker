FROM fedora:23

RUN dnf groupinstall -y "C Development Tools and Libraries"
RUN dnf install -y git cmake

RUN dnf install -y dnf-plugins-core
RUN dnf copr enable -y mstuchli/Python3.5
RUN dnf install -y python35-python3

RUN dnf clean all
