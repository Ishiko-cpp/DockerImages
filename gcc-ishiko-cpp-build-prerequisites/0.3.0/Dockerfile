FROM gcc:12.1.0 as build

WORKDIR /projects

RUN git clone https://github.com/ishiko-cpp/Kitware_CMake.git CMake
RUN cd CMake && ./bootstrap --prefix=/projects/output && make && make install

WORKDIR /projects

RUN apt-get update
RUN apt-get -y install python-dev

RUN wget https://boostorg.jfrog.io/artifactory/main/release/1.78.0/source/boost_1_78_0.tar.bz2
RUN tar xjf boost_1_78_0.tar.bz2

WORKDIR /projects/boost_1_78_0

RUN ./bootstrap.sh --prefix=/projects/output
RUN ./b2 install

FROM gcc:12.1.0
COPY --from=build /projects/output /usr/local
RUN ldconfig

WORKDIR /ishiko/cpp/fmtlib

RUN git clone https://github.com/ishiko-third-party/fmtlib_fmt.git fmt
RUN cd fmt && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/cpp/randombit

ENV ISHIKO_CPP_THIRD_PARTY_BOTAN=/ishiko/cpp/randombit/botan
RUN git clone https://github.com/ishiko-third-party/randombit_botan.git botan
RUN cd botan && git checkout 2.19.1 && python3 configure.py --prefix=${ISHIKO_CPP_THIRD_PARTY_BOTAN=/ishiko/cpp/randombit/botan} --disable-shared-library && make && make check && make install

WORKDIR /ishiko/cpp

ENV ISHIKO_CPP_THIRD_PARTY_PUGIXML=/ishiko/cpp/pugixml
RUN git clone https://github.com/ishiko-third-party/pugixml.git

WORKDIR /ishiko/cpp/no1msd

RUN git clone https://github.com/ishiko-third-party/no1msd_mstch.git mstch
RUN cd mstch && mkdir build && cd build && cmake .. && make && make install
