Irrlicht Port to vcpkg
======================

This is a port of irrlicht to vcpkg (https://github.com/Microsoft/vcpkg/)

Usage:
------
1. create a new folder in vcpkg-root/ports/ called irrlicht
2. Copy the files `CONFIG`,`portfile.cmake`,`CMakeLists.txt` to that.
3. Use vcpkg as common e.g. `vcpkg install irrlicht` (for x86, dynamic) or `vcpkg install irrlicht:x64-windows-static` (for x64 static)
4. In your programs CMakeLists.txt just use `FIND_PACKAGE(irrlicht)` and use it like any other lib

The Irrlicht sourcecode an the dependencies zlib, libpng, libjpeg, and bzip2 will then automatically downloaded, built and installed to the correct folder.

It is also possible to use vcpkg install irrlicht[fast-fpu] to build with fast math.

If this is tested well and works fine, ill consider creating a Pull Request to https://github.com/Microsoft/vcpkg/ so you dont need the steps 1 & 2 

Thanks to Darktib for creating the CMakeLists.txt for Irrlicht. (http://irrlicht.sourceforge.net/forum/viewtopic.php?f=9&t=50774)
