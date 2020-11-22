编译构建系统: cmake
基础库: boost
日志库:
    log4cpp
    glog :
        https://github.com/google/glog
        sudo apt-get install libgoogle-glog-dev

配置库: libconfig

命令行参数解析库:
    Clara, https://github.com/catchorg/Clara,deprecated
    https://github.com/bfgroup/Lyra
    /usr/lyra/include -> /home/ecnu/project/opensource/Lyra/include/
    gflags库:
        sudo apt-get install -y libgflags-dev

格式化输出:
    fmtlib, https://github.com/fmtlib/fmt
    /usr/fmt/include -> /home/ecnu/project/opensource2/fmt-7.1.2/include/
    /usr/fmt/lib -> /home/ecnu/project/opensource2/fmt-7.1.2/lib/

rpc 库: brpc
tcmalloc库:

gtest:


Issue:
    使用的各个基础库版本管理?
