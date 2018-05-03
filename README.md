# experimental_fastrtps

* Install version of cmake > 3.6 from source following https://cmake.org/install/. (This integrates clang-tidy already. By default Ubuntu 16.04 provides cmake-3.5.1)

* Install latest clang tools
```
sudo add-apt-repository 'deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial main'
wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key|sudo apt-key add -
sudo apt-get install clang-tidy-6.0 clang-format-6.0 clang-6.0
```
* Build
```
mkdir build
cd build
cmake ..
make -j8
```
