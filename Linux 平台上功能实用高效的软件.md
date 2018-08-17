Linux 平台上功能实用高效的软件
==========================

## Apps

### Albert - 快速启动器，类似于 macOS 的 Alfred

[项目主页](https://albertlauncher.github.io)

__Fedora 安装：__

```
sudo yum install muParser muParser-devel
sudo yum install pybind11-devel python3-pybind11
sudo dnf install python3-devel
git clone --recursive https://github.com/albertlauncher/albert.git
mkdir albert-build
cd albert-build
cmake ../albert -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Debug
make
sudo make install
```

报错：

1. `albert/plugins/virtualbox/src/vm.h:21:10: 致命错误：VirtualBox_XPCOM.h：No such file or directory`

解决：cmake ../albert -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Debug -DBUILD_VIRTUALBOX=Off
