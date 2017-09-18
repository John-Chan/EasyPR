CMake可以根据CMakeLists产生IDE特定的工程文件,以VC为例

```
mkdir _build
cd _build
set OPENCV_INSTALL_DIR=D:\shared\sdk-dir\opencv\3.2.0\build
cmake -G "Visual Studio 14 2015 Win64" ..
```
上述命令先指定openCV的安装路径(你从[官方下载网站](http://opencv.org/releases.html)下载后,在本机的安装位置),然后生成VC2015(64位,因为openCV库是64位的)工程文件.
> 具体参考 [cmake-generators](https://cmake.org/cmake/help/v3.4/manual/cmake-generators.7.html)
然后用VS打开_build目录下的sln文件即可.
