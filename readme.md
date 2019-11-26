# Human Detection Module
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
[![Build Status](https://travis-ci.org/Achalpvyas/PerceptionModule.svg?branch=GMock_Extra_Credit)](https://travis-ci.org/Achalpvyas/PerceptionModule)
[![Coverage Status](https://coveralls.io/repos/github/Achalpvyas/PerceptionModule/badge.svg?branch=master)](https://coveralls.io/github/Achalpvyas/PerceptionModule?branch=master)s

## License

- This module has been developed under the 3-Clause BSD License.
- Please go through the [*LICENSE*](https://github.com/urastogi885/humanDetectionModule/blob/phase1/LICENSE)
file before cloning the repository.

## Install OpenCV

- The module utilizes features of OpenCV.
- Run the commands below to install OpenCV before cloning the repository:
    - Update your system:
    ```shell script
    sudo apt update
    sudo apt upgrade
    ```
  
    - Install OpenCV Dependencies:  
    ```shell script
    sudo apt install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev
    sudo apt install python3.5-dev python3-numpy libtbb2 libtbb-dev
    sudo apt install libjpeg-dev libpng-dev libtiff5-dev libjasper-dev libdc1394-22-dev libeigen3-dev libtheora-dev libvorbis-dev libxvidcore-dev libx264-dev sphinx-common libtbb-dev yasm libfaac-dev libopencore-amrnb-dev libopencore-amrwb-dev libopenexr-dev libgstreamer-plugins-base1.0-dev libavutil-dev libavfilter-dev libavresample-dev
    ```
  
    - Install OpenCV:
    ```shell script
    git clone https://github.com/opencv/opencv.git
    cd opencv 
    git checkout 3.3.0 
    cd ..
    git clone https://github.com/opencv/opencv_contrib.git
    cd opencv_contrib
    git checkout 3.3.0
    cd ..
    cd opencv
    mkdir build
    cd build
    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D INSTALL_C_EXAMPLES=ON -D WITH_TBB=ON -D WITH_V4L=ON -D WITH_QT=ON -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules -D BUILD_EXAMPLES=ON ..
    make -j$(nproc)
    sudo make install
    sudo /bin/bash -c 'echo "/usr/local/lib" > /etc/ld.so.conf.d/opencv.conf'
    sudo ldconfig
    ```
    
## Standard install via command-line

- Switch to the directory where you want to clone this repository
- Run the following command:
```shell script
git clone --recursive https://github.com/urastogi885/humanDetectionModule
cd humanDetectionModule/
git checkout -b GMock_Extra_Credit_UR
mkdir build
cd build/
cmake ..
make
```

## Test

Within the *build* sub-directory, run:
```shell script
./test/cpp-test
```

