FROM gcc:10.1.0 as build

RUN apt-get update
RUN apt-get -y install python-dev

RUN wget https://boostorg.jfrog.io/artifactory/main/release/1.73.0/source/boost_1_73_0.tar.bz2
RUN tar xjf boost_1_73_0.tar.bz2

WORKDIR boost_1_73_0

RUN ./bootstrap.sh --prefix=/boost/install
RUN ./b2 install

FROM gcc:10.1.0
COPY --from=build /boost/install /usr/local
RUN ldconfig
