ZeroMQ core engine
    https://github.com/zeromq/libzmq
    //NOTE, in order to use draft API(e.g. poller), make sure .git file exist(MORE see CMakeLists.txt)
    注意DZMQ_BUILD_DRAFT_API 的编译,配置不对，编译出的符合为c++符号(should be c symbol)，可能导致链接失败
    mkdir build_cmake
    cd build_cmake
    cmake ../
    make

    libzmq.a/so
    zmq.h
    zmq_utils.h

    /usr/zmq/lib -> /home/ecnu/project/opensource2/zeromq-4.3.3/build_cmake/lib/
Header-only c++ binding for libzmq
    https://github.com/zeromq/cppzmq

    zmq_addon.hpp/zmq.hpp

