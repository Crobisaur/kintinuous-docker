FROM nvidia/opengl:1.1-glvnd-devel-ubuntu14.04


RUN \
  apt-get update -qq && \
  apt-get upgrade -qq -y && \
  apt-get install -qq -y \
    # requirements
  cmake-qt-gui\
  git\
  build-essential\
  libusb-1.0-0-dev\
  libudev-dev\
  openjdk-7-jdk\
  freeglut3-dev\
  python-vtk\
  libvtk-java\
  libglew-dev\
  cuda-7-5\
  libsuitesparse-dev\
  openexr\
  sudo

