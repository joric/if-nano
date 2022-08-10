# IF NANO

#### 介绍
一个适用于用于zmk，软硬件兼容nice！nano的主控。
IFNANO主要参考了nice！nano的设计，重新layout为双面板，并且增加了开关功能和ipx天线插座（1代），降低了生产成本的同时提高了实用性。
目前基本功能已经完成测试，可以正常使用。

#### 电路设计
具体请看Schematic_IFNANOV5_2022-08-10.pdf文件，基本就是克隆nice！nano原版设计。
bootloader可以直接使用nice！nano的文件，测试使用的是nice_nano_bootloader-0.6.0_s140_6.1.1.hex，已经附上。


#### 焊接教程
因为空间的原因，pcb上去除了原件相关的标号丝印，所以具体原件的值和位置请参考“焊接助手”文件。
“焊接助手”文件本质是一个网页，需要用浏览器打开。

#### 使用说明
![](./img/top.png)


1.  右上角LED为红色LED，亮灯为充电状态，不亮为充满状态或者不在充电状态（未插线）。
2.  左下角LED为功能指示灯，在BL状态下会呼吸显示，正常工作状态不亮。
3.  pcb左下角多出来的一排四孔接口为SWD接口，使用jlink用来烧录bootloader程序或者擦除芯片。
4.  本设计是有两个天线，正面是贴片天线（底部，红色原件），背面是ipx一代天线座。这两个天线在使用的时候请二选一，不要同时使用。
5.  背面设计有开关，需要使用1位的贴片拨码开关。（未经测试）
6.  本设计使用的是ti bq24057充电芯片，支持4.2V锂电池，与nice！nano的一致。芯片设定在usb 500ma模式，保留了一个控制充电电流的电阻（R9 1.68K），实际测试最大保持充电电流在430ma左右，伴随一定的发热量，所以充电的时候谨慎触摸pcb板。（没有具体测试发热温度，个人估计是60度左右，工作稳定正常）
7.  32k晶振需要安装



#### 参考资料

1.  https://nicekeyboards.com/docs/nice-nano/pinout-schematic
2. https://github.com/joric/jorne/wiki

   

#### 联系:

IFKB客制化QQ群 

78769032



作者

(QQ)463365135

(email)463365135@qq.com



















![](https://files.mdnice.com/logo.svg)

请使用 **Chrome** 浏览器。

请阅读下方文本熟悉工具使用方法，本文可直接拷贝到微信中预览。

## 1 Markdown Nice 简介

- 支持自定义样式的 Markdown 编辑器
- 支持微信公众号、知乎和稀土掘金
- 欢迎扫码回复「排版」加入推文群

![](https://files.mdnice.com/pic/cd3ca20c-896f-4cfc-9bdd-c4c58e69ba26.jpg)

## 2 主题

**https://product.mdnice.com/themes/**

欢迎提交主题，提供更多文章示例~~

## 3 通用语法

### 3.1 标题

在文字写书写不同数量的`#`可以完成不同的标题，如下：

# 一级标题

## 二级标题

### 三级标题

### 3.2 无序列表

无序列表的使用，在符号`-`后加空格使用。如下：

- 无序列表 1
- 无序列表 2
- 无序列表 3

如果要控制列表的层级，则需要在符号`-`前使用空格。如下：

- 无序列表 1
- 无序列表 2
  - 无序列表 2.1
  - 无序列表 2.2

**由于微信原因，最多支持到二级列表**。

### 3.3 有序列表

有序列表的使用，在数字及符号`.`后加空格后输入内容，如下：

1. 有序列表 1
2. 有序列表 2
3. 有序列表 3

### 3.4 粗体和斜体

粗体的使用是在需要加粗的文字前后各加两个`*`。

而斜体的使用则是在需要斜体的文字前后各加一个`*`。

如果要使用粗体和斜体，那么就是在需要操作的文字前后加三个`*`。如下：

**这个是粗体**

_这个是斜体_

**_这个是粗体加斜体_**

### 3.5 链接

微信公众号仅支持公众号文章链接，即域名为`https://mp.weixin.qq.com/`的合法链接。使用方法如下所示：

对于该论述，欢迎读者查阅之前发过的文章，[你是《未来世界的幸存者》么？](https://mp.weixin.qq.com/s/s5IhxV2ooX3JN_X416nidA)

### 3.6 引用

引用的格式是在符号 `>` 后面书写文字，文字的内容可以包含标题、链接、图片、粗体和斜体等。

一级引用如下：

> ### 一级引用示例
>
> 读一本好书，就是在和高尚的人谈话。 **——歌德**
>
> [Markdown Nice最全功能介绍](https://mp.weixin.qq.com/s/lM808MxUu6tp8zU8SBu3sg)
>
> ![这里写图片描述](https://files.mdnice.com/pic/cd3ca20c-896f-4cfc-9bdd-c4c58e69ba26.jpg)

当使用多个 `>` 符号时，就会变成多级引用

二级引用如下：

>> ### 二级引用示例
>
>> 读一本好书，就是在和高尚的人谈话。 **——歌德**
>
>> [Markdown Nice最全功能介绍](https://mp.weixin.qq.com/s/lM808MxUu6tp8zU8SBu3sg)
>
>> ![这里写图片描述](https://files.mdnice.com/pic/cd3ca20c-896f-4cfc-9bdd-c4c58e69ba26.jpg)

三级引用如下：

>>> ### 三级引用示例
>
>>> 读一本好书，就是在和高尚的人谈话。 **——歌德**
>
>>> [Markdown Nice最全功能介绍](https://mp.weixin.qq.com/s/lM808MxUu6tp8zU8SBu3sg)
>
>>> ![这里写图片描述](https://files.mdnice.com/pic/cd3ca20c-896f-4cfc-9bdd-c4c58e69ba26.jpg)

### 3.7 分割线

可以在一行中用三个以上的减号来建立一个分隔线，同时需要在分隔线的上面空一行。如下：

---

### 3.8 删除线

删除线的使用，在需要删除的文字前后各使用两个`~`，如下：

~~这是要被删除的内容。~~

### 3.9 表格

可以使用冒号来定义表格的对齐方式，如下：

| 姓名       | 年龄 |         工作 |
| :--------- | :--: | -----------: |
| 小可爱     |  18  |     吃可爱多 |
| 小小勇敢   |  20  |   爬棵勇敢树 |
| 小小小机智 |  22  | 看一本机智书 |

宽度过长的表格可以滚动，可在自定义主题中调节宽度：

| 姓名       | 年龄 |         工作 |      邮箱       |    手机     |
| :--------- | :--: | -----------: | :-------------: | :---------: |
| 小可爱     |  18  |     吃可爱多 | lovely@test.com | 18812345678 |
| 小小勇敢   |  20  |   爬棵勇敢树 | brave@test.com  | 17712345678 |
| 小小小机智 |  22  | 看一本机智书 | smart@test.com  | 16612345678 |

### 3.10 图片

插入图片，如果是行内图片则无图例，否则有图例，格式如下：

![这里写图片描述](https://files.mdnice.com/pic/cd3ca20c-896f-4cfc-9bdd-c4c58e69ba26.jpg)

可以通过在图片尾部添加宽度和高度控制图片大小，用法如下：

![同时设置宽度和高度](https://files.mdnice.com/logo.png =150x150)

![只设置宽度，推荐使用百分比](https://files.mdnice.com/logo.png =40%x)

该语法比较特殊，其他 Markdown 编辑器不完全通用。

支持 jpg、png、gif、svg 等图片格式，**其中 svg 文件仅可在微信公众平台中使用**，svg 文件示例如下：

![](https://files.mdnice.com/i-am-svg.svg)

- 支持图片**拖拽和截图粘贴**到编辑器中上传，上传时使用当前选择的图床。
- 可使用**格式->图片**上传本地图片，网站目前支持「图壳」图床，失败率低，但是只可保存一天用于排版

**注：仅支持 https 的图片，图片粘贴到微信、知乎或掘金时会自动上传其服务器，不必担心使用上述图床会导致图片丢失**。

图片还可以和链接嵌套使用，能够实现推荐卡片的效果，用法如下：

[![Markdown Nice 最全功能介绍](https://files.mdnice.com/dance.gif)](https://mp.weixin.qq.com/s/lM808MxUu6tp8zU8SBu3sg)

## 4. 特殊语法

### 4.1 脚注

> 支持平台：微信公众号、知乎。

脚注与链接的区别如下所示：

```markdown
链接：[文字](链接)
脚注：[文字](脚注解释 "脚注名字")
```

有人认为在[大前端时代](https://en.wikipedia.org/wiki/Front-end_web_development "Front-end web development")的背景下，移动端开发（Android、IOS）将逐步退出历史舞台。

[全栈工程师](是指掌握多种技能，并能利用多种技能独立完成产品的人。 "什么是全栈工程师")在业务开发流程中起到了至关重要的作用。

脚注内容请拉到最下面观看。

### 4.2 代码块

> 支持平台：微信公众号、知乎。

如果在一个行内需要引用代码，只要用反引号引起来就好，如下：

Use the `printf()` function.

在需要高亮的代码块的前一行及后一行使用三个反引号，同时**第一行反引号后面表示代码块所使用的语言**，如下：

```java
// FileName: HelloWorld.java
public class HelloWorld {
  // Java 入口程序，程序从此入口
  public static void main(String[] args) {
    System.out.println("Hello,World!"); // 向控制台打印一条语句
  }
}
```

支持以下语言种类：

```
bash
clojure，cpp，cs，css
dart，dockerfile, diff
erlang
go，gradle，groovy
haskell
java，javascript，json，julia
kotlin
lisp，lua
makefile，markdown，matlab
objectivec
perl，php，python
r，ruby，rust
scala，shell，sql，swift
tex，typescript
verilog，vhdl
xml
yaml
```

如果想要更换代码主题，可在上方挑选，不支持代码主题自定义。

其中**微信代码主题与微信官方一致**，有以下注意事项：

- 带行号且不换行，代码大小与官方一致
- 需要在代码块处标志语言，否则无法高亮
- 粘贴到公众号后，用鼠标点代码块内外一次，完成高亮

diff 不能同时和其他语言的高亮同时显示，且需要调整代码主题为微信代码主题以外的代码主题才能看到 diff 效果，使用效果如下:

```diff
+ 新增项
- 删除项
```

**其他主题不带行号，可自定义是否换行，代码大小与当前编辑器一致**

### 4.3 数学公式

> 支持平台：微信公众号、知乎。

行内公式使用方法，比如这个化学公式：$\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$

块公式使用方法如下：

$$H(D_2) = -\left(\frac{2}{4}\log_2 \frac{2}{4} + \frac{2}{4}\log_2 \frac{2}{4}\right) = 1$$

矩阵：

$$
  \begin{pmatrix}
  1 & a_1 & a_1^2 & \cdots & a_1^n \\
  1 & a_2 & a_2^2 & \cdots & a_2^n \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  1 & a_m & a_m^2 & \cdots & a_m^n \\
  \end{pmatrix}
$$

公式由于微信不支持，目前的解决方案是转成 svg 放到微信中，无需调整，矢量不失真。

目前测试如果公式量过大，在 Chrome 下会存在粘贴后无响应，但是在 Firefox 中始终能够成功。

### 4.4 TOC

> 支持平台：微信公众号、知乎。

TOC 全称为 Table of Content，列出全部标题。由于示例标题过多，需要使用将下方代码段去除即可。

```
[TOC]
```

由于微信只支持到二级列表，本工具仅支持二级标题和三级标题的显示。

### 4.5 注音符号

> 支持平台：微信公众号。

支持注音符号，用法如下：

Markdown Nice 这么好用，简直是{喜大普奔|hē hē hē hē}呀！

### 4.6 横屏滑动幻灯片

> 支持平台：微信公众号。

通过`<![](url),![](url)>`这种语法设置横屏滑动滑动片，具体用法如下：

<![蓝1](https://files.mdnice.com/blue.jpg),![绿2](https://files.mdnice.com/green.jpg),![红3](https://files.mdnice.com/red.jpg)>

### 4.7 容器块

> 支持平台：微信公众号。

通过`::: block-1`开头，`:::`结尾，来设置容器块，容器块内可以使用任意 markdown 语法，容器块内显示样式可自定义，不会被外部干扰

目前仅支持三种容器块，`block-1`、`block-2`和`block-3`

::: block-1
### 容器块 1 示例

> 读一本好书，就是在和高尚的人谈话。 **——歌德**
> :::

::: block-2
### 容器块 2 示例

> 读一本好书，就是在和高尚的人谈话。 **——歌德**
> :::

::: block-3
### 容器块 3 示例

> 读一本好书，就是在和高尚的人谈话。 **——歌德**
> :::

### 4.8 分列

> 支持平台：微信公众号。

对于需要 2 列展示的内容，可以通过分列语法实现，可以设置左右比例，不设置时默认各为50%，示例如下：

:::: column
::: column-left

**左边的内容**

![左边的图片](https://files.mdnice.com/blue.jpg)

:::
::: column-right

**右边的内容**

![右边的图片](https://files.mdnice.com/green.jpg)

:::
::::

设置百分比示例如下：

:::: column
::: column-left 30%

**左边的内容**

![左边的图片](https://files.mdnice.com/blue.jpg)

:::
::: column-right 70%

**右边的内容**

![右边的图片](https://files.mdnice.com/green.jpg)

:::
::::

## 5 其他语法

### 5.1 HTML

支持原生 HTML 语法，请写内联样式，如下：

<span style="display:block;text-align:right;color:orangered;">橙色居右</span>
<span style="display:block;text-align:center;color:orangered;">橙色居中</span>

### 5.2 UML

不支持，推荐使用开源工具`https://draw.io/`制作后再导入图片

### 5.3 更多文档

更多文档请参考 [mdnice 产品主页](https://product.mdnice.com/articles/ "更多文档")