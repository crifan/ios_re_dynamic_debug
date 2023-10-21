# lldb+debugserver

iOS逆向时，调试代码逻辑的常用调试工具之一是：命令行的`lldb + debugserver`

* 概述
  * 用`codesign`/`ldid`给`debugserver`重签名，支持任意进程可调试后，放到`/usr/bin/debugserver`，即可启动iPhone端的`debugserver`和Mac端的`lldb`去调试iOS的app的进程了
* 详见
  * [iOS逆向调试：debugserver+lldb](https://book.crifan.org/books/ios_re_debug_debugserver_lldb/website/)
