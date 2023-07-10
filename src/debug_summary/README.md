# 动态调试心得

TODO：

* 动态调试
  * 【已解决】iOS逆向心得：如何从对x8的adrp和ldr计算出对应的qword字符串值
  * 【整理】iOS逆向调试心得：bool等变量类型
  * 【整理】iOS逆向心得：变量类型是bool类型
* 类
  * 【整理】iOS逆向心得：类的属性字段偏移量计算要加上isa的父类
  * 【整理】iOS逆向心得：打印ObjC类的属性
  * 【已解决】iOS逆向：写hook代码时打印出类的私有属性变量值的类型
  * 【整理】iOS逆向调试心得：给类的属性去设置值以及如何计算类的属性的偏移量
  * 【整理】iOS逆向心得：通过查看类的地址保存的值找到值和属性字段的偏移量和对应关系
* 函数
  * 【整理】iOS逆向调试心得：bl函数调用和返回常见逻辑
  * 【整理】iOS逆向心得：ObjC函数调用时参数顺序和汇编代码中寄存器传递的参数顺序不一致
  * 【整理】iOS逆向lldb调试心得：iOS的ObjC的无名汇编跳板函数
    * 相关
      * 【已解决】clang中的__cdecl和支持哪些调用规范
      * 【已解决】微软的调用规范的参数传递和命名规范
      * 【已解决】iOS中调用asm汇编关键字：asm __asm __asm__和volatile __volatile__
      * 【已解决】XCode的断点条件判断中如何获取iOS的ObjC函数的参数值
* 计算类的属性的偏移量
  * 【已解决】调试寻找HAMPlayerInternal的_currentTime中字段的偏移量
  * 【整理】iOS逆向心得：通过查看类的地址保存的值找到值和属性字段的偏移量和对应关系
  * 【已解决】iOS逆向：写hook代码时打印出类的私有属性变量值的类型
  * 【整理】iOS逆向心得：类的属性字段偏移量计算要加上isa的父类
* C++
  * 【整理】iOS逆向心得：Cronet相关的C++的struct结构体类的属性和函数的偏移量计算逻辑
  * 【已解决】iOS逆向：IDA中如何逆向分析C++的vtable
  * 【整理】iOS逆向涉及内容：C++中的vtable
* 其他
  * 【已解决】iOS逆向：查看NSMutableURLRequest的HTTPBody的data
  * 【已解决】Xcode中调试iOS的app再次报错：Thread EXC_BREAKPOINT code 1 subcode 0x1bf09c598

---

iOS逆向的动态调试，有很多心得，整理如下。
