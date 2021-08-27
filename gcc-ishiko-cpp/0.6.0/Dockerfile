FROM ishiko/gcc-boost:11.1.0-1.76.0

ENV ISHIKO_CPP=/ishiko/cpp
ENV ISHIKO_CPP_THIRD_PARTY_PUGIXML=/ishiko/cpp/pugixml

WORKDIR /ishiko/cpp/Kitware

RUN git clone https://github.com/ishiko-cpp/Kitware_CMake.git CMake
RUN cd CMake && ./bootstrap && make && make install

WORKDIR /ishiko/cpp/KjellKod

RUN git clone https://github.com/ishiko-cpp/KjellKod_g3log.git g3log
RUN cd g3log && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/cpp

RUN git clone https://github.com/ishiko-cpp/botan.git
RUN cd botan && python3 configure.py && make && make check && make install

RUN git clone https://github.com/ishiko-cpp/pugixml.git

RUN git clone https://github.com/ishiko-cpp/base-platform.git
RUN cd base-platform/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/errors.git
RUN cd errors/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/logging.git
RUN cd logging/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/types.git
RUN cd types/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/collections.git
RUN cd collections/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/text.git
RUN cd text/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/process.git
RUN cd process/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/filesystem.git
RUN cd filesystem/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/diff.git
RUN cd diff/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/tests.git
RUN cd tests/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/terminal.git
RUN cd terminal/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/user-tasks.git
RUN cd user-tasks/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/uuids.git
RUN cd uuids/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/csv.git
RUN cd csv/build/gnumake && make

WORKDIR /
