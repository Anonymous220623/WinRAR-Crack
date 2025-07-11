# WinRAR-Crack

> [!WARNING]
> WinRAR 的唯一官网是：[https://www.rarlab.com](https://www.rarlab.com)，请勿轻易相信其他 WinRAR 软件代理公司的网站内容，
> 如果你需要了解更详细的信息，请参见 [WinRAR 的维基百科页面](https://zh.wikipedia.org/zh-cn/WinRAR)（无法正常访问维基百科的大陆用户请看下面的网页截图）。
> 
> ![image](https://github.com/user-attachments/assets/add2fda3-5674-4022-8f6d-f7515b104149)

## 前言

WinRAR 一直是全世界电脑用户常用的压缩软件。
正因如此，WinRAR 的开发团队 RarLab 会在世界各地寻找当地的**软件代理公司**给 WinRAR 做**软件翻译**和**宣传推广**。
但是，有一家来自中国大陆的公司打着【官网】的旗号，在 WinRAR 的主程序中插入他们自己的广告，
即使用户在他们的【官网】上购买了 WinRAR，广告仍然**无法去除**。
更离谱的是，这个【官网】的**备案号还是假的**！

这个所谓的【官网】就是：[winrar.com.cn](https://www.winrar.com.cn/) ，包括我在内的许多用户，都曾经不止一次地上过它的当。

https://github.com/user-attachments/assets/e242a271-58cb-4195-9bc1-14c93e892778

本人十分看不惯国内软件代理公司欺诈用户的行为，因此设立此仓库，还给用户一个【不流氓】的 WinRAR。

## 已去除广告并激活的 WinRAR 简体中文版软件下载地址

- GitHub Release：https://github.com/Anonymous220623/WinRAR-Crack/releases

### 可用的版本

| 版本号 | 可用架构 | 下载地址  |
|   --   |  --      |   --      |
| v7.00 | x32/x64 | [GitHub Release](https://github.com/Anonymous220623/WinRAR-Crack/releases/tag/v7.00) |
| v7.01 | x32/x64 | [GitHub Release](https://github.com/Anonymous220623/WinRAR-Crack/releases/tag/v7.01) |
| v7.10 | x64     | [GitHub Release](https://github.com/Anonymous220623/WinRAR-Crack/releases/tag/v7.10) |
| v7.11 | x64     | [GitHub Release](https://github.com/Anonymous220623/WinRAR-Crack/releases/tag/v7.11) |
| v7.12 | x64     | [GitHub Release](https://github.com/Anonymous220623/WinRAR-Crack/releases/tag/v7.12) |


如果你不信任此处提供的破解程序，请参阅下文的[破解方法](#如果我从官网上下载了-winrar-的简体中文版本那么如何去除该软件中的广告和评估版本水印)。

## 随便聊聊

如果你对 Windows PE 文件格式（具有 `*.exe`、`*.dll`、`*.sys` 等文件扩展名的文件格式）有一些基本了解，
那么你应该知道 Windows PE 文件格式中有一个叫【资源】的概念，
这些【资源】本身并不包含在程序的源代码文件中，而是通过开发者编写 `*.rc`（Windows 资源源码文件扩展名）文件
或是使用 Visual Studio 生成 rc 文件，
再将 rc 文件编译成 `*.res`（Windows 资源二进制字节码文件扩展名） 文件，
并通过链接器与其他 res 或 obj 文件链接生成 Windows PE 文件。

一些软件公司为了让他们的软件支持全球的语言，会选择将语言资源文件作为【资源】嵌入到程序文件中，WinRAR 就是这么做的。

## 如果我从【官网】上下载了 WinRAR 的简体中文版本，那么如何去除该软件中的广告和【评估版本】水印？

**备注**：为了修改程序文件中内置的【资源】文件，我们得使用 Resource Hacker 这个资源编辑器和反编译器。这是它的[官网](https://www.angusj.com/resourcehacker/)。

首先，我们先要在程序根目录下新建一个 `rarreg.key` 文件，文件内容为（在下面的密钥文件中任选一个）：


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

```
RAR registration data
F黵 Abonnenten von TheReatekker
Unlimited Company License
UID=4e6c1650cdf8ad615ffa
64122122505ffaae408f7ad66b8bb746f58d6fa12007f52f099ed4
6c1726e2317c46bb430560fce6cb5ffde62890079861be57638717
7131ced835ed65cc743d9777f2ea71a8e32c7e593cf66794343565
b41bcf56929486b8bcdac33d50ecf77399604752331f0c57e362ab
443f1c64352b57668957fe62d07b434a2813addb4dbd3642364647
103788926272ccc3fb675e8b657f8b66c671e01419e9e361603899
c5a2af5001dd92308cfe644830edafe109c0e6cdd5864023283383
```

```
RAR registration data
WinRAR
Unlimited Company License
UID=4b914fb772c8376bf571
6412212250f5711ad072cf351cfa39e2851192daf8a362681bbb1d
cd48da1d14d995f0bbf960fce6cb5ffde62890079861be57638717
7131ced835ed65cc743d9777f2ea71a8e32c7e593cf66794343565
b41bcf56929486b8bcdac33d50ecf773996052598f1f556defffbd
982fbe71e93df6b6346c37a3890f3c7edc65d7f5455470d13d1190
6e6fb824bcf25f155547b5fc41901ad58c0992f570be1cf5608ba9
aef69d48c864bcd72d15163897773d314187f6a9af350808719796
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

## 我还做了哪些修改？

1. 将 String Table（字符串表资源）中的 `68:2052` 项替换为以下内容：

   （更改了资源 ID 为 1080、1081、1083 的字符串）

   ```
   STRINGTABLE
   LANGUAGE LANG_CHINESE, SUBLANG_CHINESE_SIMPLIFIED
   {
   1080, 	"了解 WinRAR"
   1081, 	"https://www.rarlab.com"
   1082, 	"WinRAR 在线购买"
   1083, 	"https://www.rarlab.com"
   1085, 	"高级自解压选项"
   }
   ```

2. 将 Dialog（对话框资源）中的 `ABOUTRARDLG:2052` 项替换为以下内容：

   （更改了第 11 和 12 行）

   ```
   ABOUTRARDLG DIALOGEX 86, 26, 310, 210
   STYLE DS_SHELLFONT | DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
   CAPTION "关于 WinRAR 简体中文版"
   LANGUAGE LANG_CHINESE, SUBLANG_CHINESE_SIMPLIFIED
   FONT 8, "MS Shell Dlg 2"
   {
      CONTROL "", 109, STATIC, SS_BITMAP | SS_NOTIFY | SS_REALSIZEIMAGE | WS_CHILD | WS_VISIBLE, 11, 10, 175, 32 
      CONTROL "WinRAR 压缩管理软件", 107, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 60, 135, 8 
      CONTROL "版权所有 1993-%d", 108, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 71, 135, 8 
      CONTROL "全球发行商 win.rar GmbH", 113, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 82, 135, 8 
      CONTROL "不要相信任何【中国总代理】！", 114, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 104, 152, 16 
      CONTROL "唯一官网：www.rarlab.com", 105, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 117, 135, 8 
      CONTROL "作者: Alexander L. Roshal", -1, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 128, 135, 8 
      CONTROL "", 106, STATIC, SS_LEFT | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 139, 135, 16 
      CONTROL "", -1, STATIC, SS_ETCHEDHORZ | WS_CHILD | WS_VISIBLE, 11, 156, 135, 1 
      CONTROL "", 101, BUTTON, BS_OWNERDRAW | WS_CHILD | WS_VISIBLE | WS_TABSTOP, 148, 59, 40, 40 
      CONTROL "非商业个人版", 102, STATIC, SS_LEFTNOWORDWRAP | SS_NOPREFIX | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 161, 242, 8 
      CONTROL "", 103, STATIC, SS_LEFT | SS_NOPREFIX | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 169, 242, 16 
      CONTROL "", 104, STATIC, SS_LEFTNOWORDWRAP | SS_NOPREFIX | WS_CHILD | WS_VISIBLE | WS_GROUP, 11, 185, 242, 8 
      CONTROL "", -1, STATIC, SS_ETCHEDHORZ | WS_CHILD | WS_VISIBLE, 11, 197, 135, 1 
      CONTROL "确定", 1, BUTTON, BS_DEFPUSHBUTTON | WS_CHILD | WS_VISIBLE | WS_TABSTOP, 214, 9, 84, 14 
      CONTROL "许可(&L)", 110, BUTTON, BS_PUSHBUTTON | WS_CHILD | WS_VISIBLE | WS_TABSTOP, 214, 26, 84, 14 
      CONTROL "致谢(&A)", 111, BUTTON, BS_PUSHBUTTON | WS_CHILD | WS_VISIBLE | WS_TABSTOP, 214, 43, 84, 14 
      CONTROL "主页(&H)", 112, BUTTON, BS_PUSHBUTTON | WS_CHILD | WS_VISIBLE | WS_TABSTOP, 214, 60, 84, 14 
   }
   ```
