FROM ishiko/gcc-ishiko-cpp-build-prerequisites:0.2.0

ENV ISHIKO_CPP=/ishiko/cpp
ENV ISHIKO_CPP_THIRD_PARTY_PUGIXML=/ishiko/cpp/pugixml

WORKDIR /ishiko/cpp/fmtlib
          
RUN git clone https://github.com/ishiko-third-party/fmtlib_fmt.git fmt
RUN cd fmt && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/cpp/KjellKod

RUN git clone https://github.com/ishiko-third-party/KjellKod_g3log.git g3log
RUN cd g3log && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/cpp/randombit

ENV ISHIKO_CPP_THIRD_PARTY_BOTAN=/ishiko/cpp/randombit/botan
RUN git clone https://github.com/ishiko-third-party/randombit_botan.git botan
RUN cd botan && git checkout 2.17.3 && python3 configure.py --prefix=${ISHIKO_CPP_THIRD_PARTY_BOTAN=/ishiko/cpp/randombit/botan} --disable-shared-library && make && make check && make install

WORKDIR /ishiko/cpp

RUN git clone https://github.com/ishiko-third-party/pugixml.git

WORKDIR /ishiko/cpp/no1msd

RUN git clone https://github.com/ishiko-third-party/no1msd_mstch.git mstch
RUN cd mstch && mkdir build && cd build && cmake .. && make && make install

WORKDIR /ishiko/cpp

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

RUN git clone https://github.com/ishiko-cpp/time.git
RUN cd time/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/process.git
RUN cd process/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/filesystem.git
RUN cd filesystem/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/xml.git
RUN cd xml/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/hash.git
RUN cd hash/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/diff.git
RUN cd diff/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/configuration.git
RUN cd configuration/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/test-framework.git
RUN cd test-framework/core/build/gnumake && make
RUN cd test-framework/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/crypto.git
RUN cd crypto/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/terminal.git
RUN cd terminal/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/user-tasks.git
RUN cd user-tasks/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/uuids.git
RUN cd uuids/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/networking.git
RUN cd networking/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/http.git
RUN cd http/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/csv.git
RUN cd csv/build/gnumake && make

WORKDIR /
