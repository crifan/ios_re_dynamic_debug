# Cycript的基本用法

```bash
cycript -p PID_or_AppName
```

进入`cy#`开头的命令行界面，即表示注入成功，可以开始调试了

## Cycript中常用命令

### 调试ObjC对象的命令

```bash
[UIApplication sharedApplication]

UIApp.keyWindow.recursiveDescription().toString()

var topView = [[[[UIApplication sharedApplication] keyWindow] subviews] lastObject]
[topView recursiveDescription].toString()

var p = new Instance(0x157d1e200)
```

### 打印最顶层页面/窗口

背景知识是，iOS的ObjC的获取最顶层的窗口：

```bash
[[[[UIApplication sharedApplication] keyWindow] subviews] lastObject]
```

放到Cycript中：

```bash
[[[[[UIApplication sharedApplication] keyWindow] subviews] lastObject] recursiveDescription].toString()
```

进一步优化：

写成变量，便于后续引用：

```bash
var topView = [[[[UIApplication sharedApplication] keyWindow] subviews] lastObject]
[topView recursiveDescription].toString()
```

### 打印页面详情

已有视图view：

```bash
cy [[[[UIApplication sharedApplication] keyWindow] subviews] lastObject]
#"<UITransitionView: 0x11f9059e0; frame = (0 0; 375 667); autoresize = W+H; layer = <CALayer: 0x280129300>>"
```

去打印页面详情，以字符串输出，是：

* 先：`recursiveDescription`
* 再：`toString`

即：

```bash
var topView = [[[[UIApplication sharedApplication] keyWindow] subviews] lastObject]
[topView recursiveDescription].toString()
```
