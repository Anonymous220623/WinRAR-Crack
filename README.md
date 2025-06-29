# WinRAR-Crack

WinRAR 一直是全世界电脑用户常用的压缩软件。
正因如此，WinRAR 的开发团队 RarLab 会在世界各地寻找当地的软件代理公司给 WinRAR 做软件翻译和宣传推广。
但是，有一家来自中国大陆的公司打着【官网】的旗号，在 WinRAR 的主程序中插入他们自己的广告，
即使用户在他们的【官网】上购买了 WinRAR，广告仍然无法去除。
更离谱的是，这个【官网】的备案号还是假的！

这个所谓的【官网】就是：[winrar.com.cn](https://www.winrar.com.cn/) ，包括我在内的许多用户，都曾经不止一次地上过它的当。

https://github.com/user-attachments/assets/e242a271-58cb-4195-9bc1-14c93e892778

本人十分看不惯国内软件代理公司欺诈用户的行为，因此设立此仓库，还给用户一个【不流氓】的 WinRAR。

## 软件下载地址

- GitHub：https://github.com/Anonymous220623/WinRAR-Crack/releases

## 前言

如果你对 Windows PE 文件格式（具有 `*.exe`、`*.dll`、`*.sys` 等文件扩展名的文件格式）有一些基本了解，
那么你应该知道 Windows PE 文件格式中有一个叫【资源】的概念，
这些【资源】本身并不包含在程序的源代码文件中，而是通过开发者编写 `*.rc`（Windows 资源源码文件扩展名）文件
或是使用 Visual Studio 生成 rc 文件，
再将 rc 文件编译成 `*.res`（Windows 资源二进制字节码文件扩展名） 文件，
并通过链接器与其他 res 或 obj 文件链接生成 Windows PE 文件。

一些软件公司为了让他们的软件支持全球的语言，会选择将语言资源文件作为【资源】嵌入到程序文件中，WinRAR 就是这么做的。

## 如何去除 WinRAR 简体中文版中的广告？

为了修改程序文件中内置的【资源】文件，我们得使用 Resource Hacker 这个资源编辑器和反编译器。这是它的[官网](https://www.angusj.com/resourcehacker/)。

首先，我们先要在程序根目录下新建一个 `rarreg.key` 文件，文件内容为：

```
RAR registration data
Federal Agency for Education
1000000 PC usage license
UID=b621cca9a84bc5deffbf
6412612250ffbf533df6db2dfe8ccc3aae5362c06d54762105357d
5e3b1489e751c76bf6e0640001014be50a52303fed29664b074145
7e567d04159ad8defc3fb6edf32831fd1966f72c21c0c53c02fbbb
2f91cfca671d9c482b11b8ac3281cb21378e85606494da349941fa
e9ee328f12dc73e90b6356b921fbfb8522d6562a6a4b97e8ef6c9f
fb866be1e3826b5aa126a4d2bfe9336ad63003fc0e71c307fc2c60
64416495d4c55a0cc82d402110498da970812063934815d81470829275
```

保存后，使用 Resource Hacker 打开 `WinRAR.exe`（WinRAR 主程序文件），
在左侧的资源树形列表中找到 `String Table`（字符串表资源）项并展开列表，再在展开项中找到 `80` 项（简体中文版是 `80:2052` ），将这一项的内容替换为：

```
STRINGTABLE
LANGUAGE LANG_CHINESE, SUBLANG_CHINESE_SIMPLIFIED
{
  1265, 	"当前文件夹"
  1267, 	"已选项目"
  1268, 	"已找到 %u"
  1269, 	"停止"
  1275, 	"https://www.rarlab.com"
  1276, 	"https://www.rarlab.com"
  1278, 	"https://www.rarlab.com/themes.htm"
}
```

按 F5 编译资源文件，再按 Ctrl+S 保存文件。

此时，Resource Hacker 会将原来的程序文件做一个备份（程序目录中会多出来一个 `WinRAR_original.exe`，这是原文件的备份），
打开 `WinRAR.exe`（新保存的文件），如果能正常运行，`WinRAR_original.exe` 就可以删除了。
如果无法运行，请将 `WinRAR.exe`（新保存的文件）删除，将 `WinRAR_original.exe` 重命名为 `WinRAR.exe`（初始文件名），并从头重复上述步骤。 
