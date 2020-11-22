
Notes:
    1. 库函数本身都是可重入;
    2. 调用函数操作配置文件，注意避免多个同时执行;
    3. 暂不支持异步调用(不友好)
    4. 国际化支持欠缺, UTF-8字符作为字节传输需要进行转换(iconv)
usage:

    scalar value: integer, 64-bit integer, float, double, boolean, string
        version = "1.0";
        timeout_ms = 1000;
        enable_debug = false;//TRUE/true/FALSE/false
        u

    array: a sequence of scalar type, all of which must have the same type
        ip_array = ["127.0.1", "192.168.0.1", "192.168.0.0"];
    group: a collection of setting
        application:
        {
        };
    list:  a sequency of values of any type
        list = (xx,xx);

    name is case-sensitive, alphanumberic characters, -, _, *;
    start with letter or *;
    map to c/c++:
    integer(0-9, 0xAF, +/-) -> int
    64-bit(0L) -> long long
    foating(+/-, 2.5, 1E2) -> double
    string("", "\"", "\\", "\n\t\r", "\xFF") -> const char*
    bool(true, false) -> int(C), bool(c++)
comment:
    #
    /* */
    //
    format:
        name = value; name : value;// ';' is not required
        @include "config_file_name"
        //include maximum nested level is 10

install:
    http://www.hyperrealm.com/libconfig/
    https://github.com/hyperrealm/libconfig

    https://hyperrealm.github.io/libconfig/
    more in INSTALL file of the repository
    sudo apt install autoconf
    sudo apt install libtool
    sudo apt install texinfo

    autoreconf
    ./configure
    make

    lib/libconfig.h
    lib/libconfig.h++
    ./lib/.libs/libconfig++.so
    ./lib/.libs/libconfig.so

    /usr/libconfig
        include -> /home/ecnu/project/opensource/libconfig/lib/
        lib -> /home/ecnu/project/opensource/libconfig/lib/.libs/
