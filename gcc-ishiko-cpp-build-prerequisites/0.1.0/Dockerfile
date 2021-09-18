FROM gcc:11.1.0 as build

WORKDIR /projects

RUN git clone https://github.com/ishiko-cpp/Kitware_CMake.git CMake
RUN cd CMake && ./bootstrap --prefix=/projects/output && make && make install

WORKDIR /projects

RUN apt-get update
RUN apt-get -y install python-dev

RUN wget https://boostorg.jfrog.io/artifactory/main/release/1.76.0/source/boost_1_76_0.tar.bz2
RUN tar xjf boost_1_76_0.tar.bz2

WORKDIR /projects/boost_1_76_0

RUN ./bootstrap.sh --prefix=/projects/output
RUN ./b2 install

FROM gcc:11.1.0
COPY --from=build /projects/output /usr/local
RUN ldconfig
