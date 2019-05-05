# GCC with Boost Docker Images

Configuration files for [Docker](https://www.docker.com/) images that contain [GCC](https://gcc.gnu.org/) and
the [Boost](https://www.boost.org/) libraries.

The images are available from [Docker Hub](https://hub.docker.com/r/ishikocpp/gcc-boost).

# Image Contents

The images are based on the [the official GCC Docker image](https://hub.docker.com/_/gcc) with the addition of 
the Boost libraries that are installed in /usr/local/include and /usr/local/lib.

The image uses a [multi-stage build](https://docs.docker.com/develop/develop-images/multistage-build/) to remove
the files generated during the Boost build process from the final image.

The first stage is based on the GCC Docker image. The Boost source code is downloaded from the Boost website and
then built using the Boost build scripts.

The second stage is also based on the GCC Docker image but in this stage we simply copy the Boost libraries from
the first stage to the /usr/local/include and /usr/local/lib in the final image.


# Tags

The first element of the tag is the GCC version e.g. 9.1.0 and the second element of the tag is the Boost version
e.g. 1.70.0.
