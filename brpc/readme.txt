

https://www.bookstack.cn/read/incubator-brpc/48b8de09ff568001.md

https://github.com/apache/incubator-brpc

install:
    https://github.com/apache/incubator-brpc/blob/master/docs/cn/getting_started.md

    sudo apt-get install -y git g++ make libssl-dev libgflags-dev libprotobuf-dev libprotoc-dev protobuf-compiler libleveldb-dev

    sudo apt-get install -y libgoogle-perftools-dev
    sudo apt-get install -y cmake libgtest-dev && cd /usr/src/gtest && sudo cmake . && sudo make && sudo mv libgtest* /usr/lib/ && cd -

    mkdir bld && cd bld && cmake .. && make

    /usr/brpc
        include -> /home/ecnu/project/opensource/incubator-brpc/bld/output/include/
        lib -> /home/ecnu/project/opensource/incubator-brpc/bld/output/lib/
