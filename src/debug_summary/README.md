# 动态调试心得

TODO：

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

---

iOS逆向的动态调试，有很多心得，整理如下。
