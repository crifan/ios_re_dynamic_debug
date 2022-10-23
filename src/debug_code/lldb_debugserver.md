# lldb+debugserver

TODO：

* 【已解决】把增加了权限的debugserver拷贝到越狱iPhone中
* 【已解决】debugserver带日志运行报错：Failed to open log file for writing errno 1 Operation not permitted
* 【已解决】debugserver启动iOS的app抖音报错：Segmentation fault 11
* 【已解决】用debugserver和lldb去调试iOS的app

---

iOS逆向调试代码逻辑的调试工具之一是：命令行的`lldb + debugserver`

![lldb_debugserver_arch](../assets/img/lldb_debugserver_arch.jpg)

* `debugserver`
  * 是什么：一个终端的应用
    * 也是：`XCode`去调试iOS设备中程序时候的进程名
  * 在哪里：iOS设备中
    * 位置：`/Developer/usr/bin/debugserver`
    * 注：iOS中默认没安装
      * iOS中安装`debugserver`
        * 在设备连接过一次`Xcode`，并在`Window`->`Devices`中添加此设备后
          * `debugserver`才会被`Xcode`安装到`iOS`的`/Developer/usr/bin/`下
  * 作用：作为服务端，接受来自远端的`gdb`或`lldb`的调试
    * 可以理解为：`lldb`的`server`
  * 为何需要
    * iOS中，由于App运行检测到越狱后会直接退出，所以需要通过`debugserver`来启动程序
  * 通过`debugserver`来启动程序
    * 举例
      * `debugserver -x backboard 0.0.0.0:1234 ./*`
      * `debugserver *:1234 -a "MoneyPlatListedVersion"`

从技术上，应属于：LLDB的远程调试，需要用到：`lldb-server`

* lldb-server 远程调试
  * 分2个端
    * `lldb client`
      * 运行在 local system
        * 比如`Linux`、`Mac`
    * `lldb server`
      * 不同平台
        * `Linux`和`Android`：`lldb-server`
          * 不依赖于`lldb`
            * 因为：已静态链接包含了`LLDB`的核心功能
            * 对比：`lldb`是默认是动态链接`liblldb.so`
        * `Mac`和`iOS`：`debugserver`
      * 运行在 remote system
      * 实现了remote-gdb的功能
    * 两者通讯
      * 用的是：`gdb-remote`协议
        * 一般是在TCP/IP之上运行
  * 细节详见：
    * `docs/lldb-gdb-remote.txt`
  * 资料
    * 主页
      * Remote Debugging — The LLDB Debugger
        * http://lldb.llvm.org/use/remote.html
