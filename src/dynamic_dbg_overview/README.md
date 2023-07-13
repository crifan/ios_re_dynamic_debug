# iOS逆向动态调试概览

[iOS逆向](http://book.crifan.org/books/ios_reverse_dev/website)，从`是否要运行代码`的角度来说，分：

* 不要运行代码的：[静态分析](https://book.crifan.org/books/ios_re_static_analysis/website/)
* 要运行代码的：`动态调试`

此文主要介绍`动态调试`的相关内容：

* 输入=前提：[砸壳出的ipa](https://book.crifan.org/books/ios_re_crack_shell_ipa/website/)文件（或已把ipa安装到iOS设备中）
* 主要涉及的内容=领域
  * 调试代码逻辑
    * 常见调试工具
      * 图形界面：[Xcode + MonkeyDev](https://book.crifan.org/books/ios_re_monkeydev_debug/website/)
      * 命令行：[debugserver + lldb](../debug_code/lldb_debugserver.md)
        * [主流调试器：LLDB](https://book.crifan.org/books/popular_debugger_lldb/website/)
      * [Frida](https://book.crifan.org/books/reverse_debug_frida/website/)
      * [IDA](https://book.crifan.org/books/reverse_tool_ida/website/)
    * 涉及到的相关子领域
      * [反调试和反反调试](../anti_debug_related.md)
      * [Xcode开发：调试心得](http://book.crifan.org/books/xcode_dev_debug_summary/website/)
  * 调试界面元素
    * [Reveal](../debug_ui/reveal.md)
    * [Cycript](../debug_ui/cycript/README.md)
    * [LLDBTools](../debug_ui/lldbtools.md)
    * [chisel](../debug_ui/chisel.md)
    * [FLEX](../debug_ui/flex.md)
