FROM ishikocpp/gcc-boost:latest

WORKDIR Ishiko-Cpp

ENV ISHIKO_CPP=/Ishiko-Cpp

RUN git clone https://github.com/Ishiko-Cpp/Errors.git
RUN cd Errors/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Process.git
RUN cd Process/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/TestFramework.git
RUN cd TestFramework/Core/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/FileSystem.git
RUN cd FileSystem/Makefiles/GNUmakefile && make
