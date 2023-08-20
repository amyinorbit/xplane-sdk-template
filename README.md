X-Plane Cmake template
======================

This is an example of an X-Plane plugin project using Cmake. `CMakeLists` shows the basic steps to
using `xplm.cmake`.

In order to build your project:

````sh
$ mkdir build
$ cd build
$ cmake .. && make
````

This will create a new directory for your plugin at the project root (or if it already exists, it
will create the appropriate `lin_x64`, `win_x64`, or `mac_x64` sub-directory, matching the system
you are building for.)

In order to cross-compile for windows under linux, you can use the `XCompile.txt` toolchain file:

````sh
$ mkdir build
$ cd build
$ cmake -DCMAKE_TOOLCHAIN_FILE=../XCompile.txt \
        -DHOST=x86_64-w64-mingw32 \
		..
````

This assumes that you have the mingw-w64 toolchain installed.

License
-------

The files included in this repository are shared in the public domain.

