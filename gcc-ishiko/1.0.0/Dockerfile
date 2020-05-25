FROM ishikocpp/gcc-boost:latest

WORKDIR Ishiko-cpp

ENV ISHIKO_CPP=/Ishiko-cpp

RUN git clone https://github.com/Ishiko-Cpp/Errors.git
RUN cd Errors/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Process.git
RUN cd Process/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/TestFramework.git
RUN cd TestFramework/Core/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Collections.git
RUN cd Collections/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/FileSystem.git
RUN cd FileSystem/Makefiles/GNUmakefile && make

WORKDIR /
