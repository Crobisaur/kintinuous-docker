FROM nvidia/opengl:1.1-glvnd-devel-ubuntu14.04

ENV NVIDIA_DRIVER_CAPABILITIES ${NVIDIA_DRIVER_CAPABILITIES},display

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
  #cuda-7-5\
  libsuitesparse-dev\
  openexr\
  sudo \
  && rm -rf /var/lib/apt/lists/*

RUN sudo add-apt-repository -y ppa:v-launchpad-jochen-prickerhof-de/pcl &&\
  sudo apt-get update && \
  sudo apt-get install -y libpcl-all && \
  rm -rf /var/lib/apt/lists/*

### Gotta build pakcages OpenCV DLib, DBoW2, DLoopDetector, iSAM and Pangolin
### from source in this order because reasons

RUN git clone https://github.com/opencv/opencv.git /opt/opencv && \
  cd /opt/opencv && \
  git checkout tags/2.4.9 && \
  
RUN git clone https://github.com/dorian3d/DLib.git /opt/DLib && \
  cd /opt/DLib 


#build this junk last
RUN git clone https://github.com/mp3guy/Kintinuous.git /opt/kintinuous &&\
  cd /opt/kintinuous

