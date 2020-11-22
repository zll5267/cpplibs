c++项目的编译系统

需要支持的功能：
    1. 自动生成Makefile
    2. 配置指定include文件目录，库文件目录(.a,.so)
    3. 预编译宏配置，编译参数配置，连接参数配置
    4. UT测试支持，运行+结果展示
    5.

选择CMake原因：
    1. 过去使用过，有点使用经验
    2. 开源，自由，本身现在已经比较成熟,使用广
    3. 没有相同其他更合适的代替者

CMake:
    https://cmake.org/cmake/help/latest/guide/tutorial/index.html
    https://gitlab.kitware.com/cmake/cmake/tree/master/Help/guide/tutorial

install command:
    sudo apt install cmake

usage tips:
    cmake -DUSE_STATIC_MYFUNCTION=OFF ../
    target_include_directories(xxxx INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
    INTERFACE here means: consumer require but the producer doesn't

    include(CheckSymbolExists)
    set(CMAKE_REQUIRED_LIBRARIES "m")
    check_symbol_exists(log "math.h" HAVE_LOG)
    unset(HAVE_LOG)
    if(HAVE_LOG)
        target_link_libraries(xxx PRIVATE m)
    endif()

    target_compile_definitions(xxx PRIVATE "HAVE_LOG" "HAVE_EXP")


    module path:
             /usr/share/cmake-3.10/Modules/
             /usr/lib/x86_64-linux-gnu/cmake/
     CMAKE_SYSTEM_PREFIX_PATH/ default path used in find_library/path

    add_custome_command(OUTPUT xxxx
                        COMMAND bin xxxx
                        DEPEND bin
                       )
    CPack: use to build a installer
    CTest: test result to dashboard
