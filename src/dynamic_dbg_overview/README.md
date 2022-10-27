# iOS逆向动态调试概览

iOS逆向，从`是否要运行代码`的角度来说，分：

* 不要运行代码的：[静态分析](https://book.crifan.org/books/ios_re_static_analysis/website/)
* 要运行代码的：`动态调试`

此文主要介绍`动态调试`的相关内容：

* 输入=前提：[砸壳出的ipa](https://book.crifan.org/books/ios_re_crack_shell_ipa/website/)文件（或已把ipa安装到iOS设备中）
* 主要涉及的内容=领域
  * 调试代码逻辑
    * 常见调试工具
      * 图形界面：`Xcode + MonkeyDev`
      * 命令行：`debugserver + lldb`
      * `Frida`
      * [IDA](https://book.crifan.org/books/reverse_tool_ida/website/)
    * 涉及到的相关子领域
      * `反调试`和`反反调试`
      * Xcode调试心得
        * 【整理Book】Xcode开发：调试心得
      * [Xcode内置调试器：LLDB](https://book.crifan.org/books/xcode_debugger_lldb/website/)
  * 调试界面元素
    * `Reveal`
    * `Cycript`
    * （MonkeyDev的）`LLDBTools`
    * `chisel`
    * `FLEX`
