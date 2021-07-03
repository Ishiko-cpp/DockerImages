FROM ishiko/gcc-boost:11.1.0-1.76.0

WORKDIR ishiko/cpp

ENV ISHIKO_CPP=/ishiko/cpp
ENV ISHIKO_CPP_THIRD_PARTY_PUGIXML=/ishiko/cpp/pugixml

RUN git clone https://github.com/ishiko-cpp/botan.git
RUN cd botan && python3 configure.py && make && make check && make install

RUN git clone https://github.com/ishiko-cpp/pugixml.git

RUN git clone https://github.com/ishiko-cpp/platform.git
RUN cd platform/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/errors.git
RUN cd errors/build/gnumake && make

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

RUN git clone https://github.com/ishiko-cpp/tasks.git
RUN cd tasks/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/uuids.git
RUN cd uuids/build/gnumake && make

WORKDIR /
