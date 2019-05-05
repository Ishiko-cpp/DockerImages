FROM gcc:9 as build

RUN apt-get update
RUN apt-get -y install python-dev

RUN wget https://dl.bintray.com/boostorg/release/1.70.0/source/boost_1_70_0.tar.bz2
RUN tar xjf boost_1_70_0.tar.bz2

WORKDIR boost_1_70_0

RUN ./bootstrap.sh --prefix=/boost/install
RUN ./b2 install

FROM gcc:9
COPY --from=build /boost/install /usr/local
RUN ldconfig
