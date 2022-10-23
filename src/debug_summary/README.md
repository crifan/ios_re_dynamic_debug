# 动态调试心得

iOS逆向的动态调试，有很多心得，整理如下。

## objc_msgSend

iOS的ObjC的底层函数调用，都是通过`objc_msgSend`实现的。

iOS逆向调试期间，关于`objc_msgSend`也有很多心得，整理如下。

### 不带lldb_unnamed_symbol的无名的bl，往往是更重要的，我们所关注的objc_msgSend

折腾：
【未解决】研究抖音关注逻辑：___lldb_unnamed_symbol1588524$$AwemeCore
期间，调试到目前的心得：

如果是带`___lldb_unnamed_symbol`的写法，往往不是主要的，我们所关心的`objc_msgSend`函数

而无名的`bl`，往往是重要的，我们所关注的：`objc_msgSend`的相关调用

举例：

```nasm
    0x11427c2c8 <+336>: bl     0x115ce58fc
```

其实就是：`objc_msgSend`

而其他很多其他的bl：

```nasm
    0x11427c2b0 <+312>: bl     0x11427e920              ; ___lldb_unnamed_symbol1588573$$AwemeCore
```

只是个`jmp_objc_retain`，不是我们关注的重点。
