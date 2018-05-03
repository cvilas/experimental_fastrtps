# experimental_fastrtps

Requires clang tools version 6.0
```
sudo add-apt-repository 'deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial main'
wget -O - http://apt.llvm.org/llvm-snapshot.gpg.key|sudo apt-key add -
sudo apt-get install clang-tidy-6.0
```
The build..
```
mkdir build
cd build
cmake ..
make -j8
```
