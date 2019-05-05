# GCC with Ishiko/C++ Docker Images

Configuration files for [Docker](https://www.docker.com/) images that contain [GCC](https://gcc.gnu.org/) and
the Ishiko/C++ framework. As the Ishiko/C++ framework relies heavily on Boost the Boost libraries are also
part of the images.

The images are available from [Docker Hub](https://hub.docker.com/r/ishikocpp/gcc-ishiko).

# Image Contents

The images are based on the [the official GCC Docker image](https://hub.docker.com/_/gcc) with the addition of
- the Boost libraries, which are installed in /usr/local/include and /usr/local/lib, and
- the Ishiko/C++ framework.
