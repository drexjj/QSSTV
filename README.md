# QSSTV
QSSTV is a program for receiving and transmitting SSTV and HAMDRM (sometimes called DSSTV). It is compatible with most of MMSSTV and EasyPal

## Installation

### Dependencies 

For sBitx you can install dependencies as follows:

```
sudo apt install qmake6 pkg-config g++ libfftw3-dev qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools libhamlib++-dev libasound2-dev libopenjp2-7 libopenjp2-7-dev libv4l-dev build-essential
```

### Compile and Install
 	cd $HOME && git clone https://github.com/drexjj/QSSTV.git
	cd QSSTV
	mkdir src/build
	cd src/build
	qmake ..
	make -j2
	sudo make install

Note: make -j2, 2 is the number of cores to be used for parallel compiling. If you have more cores, use a higher number.

### Debug Compile

If you want to be able to debug the program, the simplest way is to install QtCreator and from within QtCreator open a new project and point to the qsstv.pro file. Note: you will need to install doxygen and libqwt

`sudo apt-get install doxygen libqwt-qt5-dev`

You can also run qmake with the following atributes:

`qmake CONFIG+=debug`

and use an external debugger (such as gdb)
