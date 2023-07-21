# Xcode

iOS逆向期间，对于想要调试`app`/`二进制`的代码逻辑的手段不少。

此处之所以把，看起来是单独属于 [Xcode开发：调试心得](http://book.crifan.org/books/xcode_dev_debug_summary/website/) 中的 `Xcode`，单独拿出来说，原因是：

* Xcode调试的优势
  * 是GUI图形界面的，比 [lldb+debugserver](../debug_code/lldb_debugserver.md) 更加直观和方便
* Xcode调试需要满足前提
  * `app`/`二进制`是可调试的 = 任意进程可调试

其中最重要的是：

* 要满足任意进程可调试的前提条件
  * 如何实现任意进程可调试
    * 概述
      * 如果是[XinaA15](https://book.crifan.org/books/ios_re_ios15_jailbreak/website/xinaa15/)越狱后，自动已实现任意进程可调试，无需额外操作
      * 否则就要自己手动去操作：`Mac`中用`codesign`给`app`/`二进制`重签名，替换掉iPhone中原有的`app`/`二进制`
    * 详解
      * [任意进程可调试 · iOS逆向开发：签名和权限](https://book.crifan.org/books/ios_re_codesign_ent/website/common_issue/process_debuggable/)
        * [XinaA15自带已支持](https://book.crifan.org/books/ios_re_codesign_ent/website/common_issue/process_debuggable/xinaa15_builtin.html)
        * [手动重签名](https://book.crifan.org/books/ios_re_codesign_ent/website/common_issue/process_debuggable/self_do_resign.html)
