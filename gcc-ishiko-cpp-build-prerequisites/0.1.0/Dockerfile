FROM gcc:11.1.0 as build

WORKDIR /ishiko/cpp/Kitware

RUN git clone https://github.com/ishiko-cpp/Kitware_CMake.git CMake
RUN cd CMake && ./bootstrap --prefix=/ishiko/cpp/Kitware/CMake/install && make && make install

WORKDIR /

RUN apt-get update
RUN apt-get -y install python-dev

RUN wget https://boostorg.jfrog.io/artifactory/main/release/1.76.0/source/boost_1_76_0.tar.bz2
RUN tar xjf boost_1_76_0.tar.bz2

WORKDIR boost_1_76_0

RUN ./bootstrap.sh --prefix=/boost/install
RUN ./b2 install

FROM gcc:11.1.0
COPY --from=build /boost/install /usr/local
RUN ldconfig
