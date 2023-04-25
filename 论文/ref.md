# cartographer交叉编译
## boost中的iostream库

### bzip2
更改CMakeLists.txt中的编译器位置，以及绝对位置。
####告知当前使用的是交叉编译方式，必须配置
SET(CMAKE_SYSTEM_NAME Linux)
SET(TOOLCHAIN_DIR "/home/xunxu/下载/arm64/ti")
#####指定编译工具，一定要设置
#####或交叉编译器使用绝对地址
SET(CMAKE_C_COMPILER ${TOOLCHAIN_DIR}/bin/aarch64-none-linux-gnu-gcc)
SET(CMAKE_CXX_COMPILER ${TOOLCHAIN_DIR}/bin/aarch64-none-linux-gnu-g++)
#####指定C++交叉编译器
SET(CMAKE_CXX_COMPILER ${TOOLCHAIN_DIR}/bin/aarch64-none-linux-gnu-g++)
### 参考链接：
Boost::iostreams 库编译和压缩数据流：https://www.miaokee.com/370257.html

