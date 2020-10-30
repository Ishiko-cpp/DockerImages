FROM ishikocpp/gcc-boost:10.1.0-1.73.0

WORKDIR Ishiko-cpp

ENV PUGIXML=/Ishiko-cpp/pugixml
ENV ISHIKO_CPP=/Ishiko-cpp

RUN git clone https://github.com/Ishiko-cpp/pugixml.git

RUN git clone https://github.com/Ishiko-Cpp/Platform.git

RUN git clone https://github.com/Ishiko-Cpp/Errors.git
RUN cd Errors/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Types.git
RUN cd Types/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Process.git
RUN cd Process/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/TestFramework.git
RUN cd TestFramework/Core/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Collections.git
RUN cd Collections/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/FileSystem.git
RUN cd FileSystem/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Terminal.git
RUN cd Terminal/Makefiles/GNUmakefile && make

RUN git clone https://github.com/Ishiko-Cpp/Tasks.git
RUN cd Tasks/Makefiles/GNUmakefile && make

WORKDIR /
