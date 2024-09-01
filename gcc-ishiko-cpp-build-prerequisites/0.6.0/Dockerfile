FROM gcc:14.2.0 AS build

WORKDIR /projects/Kitware

RUN git clone https://github.com/ishiko-third-party/Kitware_CMake.git CMake
RUN cd CMake && ./bootstrap --prefix=/projects/output && make && make install

WORKDIR /projects

RUN wget https://boostorg.jfrog.io/artifactory/main/release/1.86.0/source/boost_1_86_0.tar.bz2
RUN tar xjf boost_1_86_0.tar.bz2

WORKDIR /projects/boost_1_86_0

RUN ./bootstrap.sh --prefix=/projects/output
RUN ./b2 install

FROM gcc:14.2.0
COPY --from=build /projects/output /usr/local
RUN ldconfig

WORKDIR /ishiko/third-party/fmtlib

RUN git clone https://github.com/ishiko-third-party/fmtlib_fmt.git fmt
RUN cd fmt && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/third-party/randombit

ENV BOTAN_ROOT=/ishiko/third-party/randombit/botan
RUN git clone https://github.com/ishiko-third-party/randombit_botan.git botan
RUN cd botan && git checkout 2.19.1 && python3 configure.py --prefix=${BOTAN_ROOT} --disable-shared-library && make && make check && make install

WORKDIR /ishiko/third-party

ENV PUGIXML_ROOT=/ishiko/third-party/pugixml
RUN git clone https://github.com/ishiko-third-party/pugixml.git

WORKDIR /ishiko/third-party/no1msd

RUN git clone https://github.com/ishiko-third-party/no1msd_mstch.git mstch
RUN cd mstch && mkdir build && cd build && cmake .. && make && make install
