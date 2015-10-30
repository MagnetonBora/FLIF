# FLIF: Free Lossless Image Format

[![Build Status](https://travis-ci.org/FLIF-hub/FLIF.svg?branch=master)](https://travis-ci.org/FLIF-hub/FLIF)
[![Join the chat at https://gitter.im/jonsneyers/FLIF](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/jonsneyers/FLIF?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)


FLIF is a lossless image format based on MANIAC compression. MANIAC (Meta-Adaptive Near-zero Integer Arithmetic Coding) is a variant of CABAC (context-adaptive binary arithmetic coding), where the contexts are nodes of decision trees which are dynamically learned at encode time.

FLIF outperforms PNG, FFV1, lossless WebP, lossless BPG and lossless JPEG2000 in terms of compression ratio.

Moreover, FLIF supports a form of progressive interlacing (essentially a generalization/improvement of PNG's Adam7) which means that any prefix (e.g. partial download) of a compressed file can be used as a reasonable lossy encoding of the entire image.

For more information on FLIF, visit http://flif.info

* * *

###Build Instructions

**GNU/Linux**

* Install the dependencies:
  * for the encoder/decoder: `sudo apt-get install libpng-dev`
  * for the viewer: `sudo apt-get install libsdl2-dev`
* Navigate to the FLIF directory and run `make` to build `flif`
  * `make libflif.so` to build the shared library
  * `make viewflif` to build the example viewer
* `sudo make install` if you want to install it globally

**Windows**

* Install Visual Studio
  ([VS Community 2015](https://www.visualstudio.com/en-us/products/free-developer-offers-vs.aspx)
  is free for open source projects)
* Open the `build\MSVC` folder and Double click the `dl_make_vs.bat`. This will download required libraries and run `nmake` to build `flif.exe`
  * `nmake libflif.dll` to build the shared library
  * `nmake viewflif.exe` to build the example viewer

**OS X**

* Install [homebrew](http://brew.sh)
* Install kegs named `pkg-config` and `libpng`
* Run `make` in the FLIF directory


* * *

###Pre-Built Binaries

These will be available on the Release page

* https://github.com/FLIF-hub/FLIF/releases

* * *

###Related Projects

* **[Poly-FLIF](https://uprootlabs.github.io/poly-flif)** - A javascript polyfill that allows you to use FLIF files in the browser.
* **[UGUI: FLIF](https://github.com/FLIF-hub/UGUI_FLIF/releases)** - A GUI that allows you to convert and view FLIF files.
