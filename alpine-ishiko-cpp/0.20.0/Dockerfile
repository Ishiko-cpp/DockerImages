FROM ishiko/alpine-ishiko-cpp-build-prerequisites:0.5.0

ENV ISHIKO_CPP_ROOT=/ishiko/cpp

WORKDIR /ishiko/cpp

RUN git clone https://github.com/ishiko-cpp/base-platform.git
RUN cd base-platform/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/errors.git
RUN cd errors/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/memory.git
RUN cd memory/build/gnumake && make

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

RUN git clone https://github.com/ishiko-cpp/concurrency.git
RUN cd concurrency/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/process.git
RUN cd process/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/io.git
RUN cd io/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/filesystem.git
RUN cd filesystem/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/xml.git
RUN cd xml/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/json.git
RUN cd json/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/yaml.git
RUN cd yaml/build/gnumake && make

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

RUN git clone https://github.com/ishiko-cpp/workflows.git
RUN cd workflows/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/uuids.git
RUN cd uuids/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/networking.git
RUN cd networking/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/http.git
RUN cd http/build/gnumake && make

RUN git clone https://github.com/ishiko-cpp/csv.git
RUN cd csv/build/gnumake && make

WORKDIR /
