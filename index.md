title: Python 基础教学
speaker: TonyCrane
css: 
    - https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;600&family=Source+Code+Pro&family=JetBrains+Mono:ital,wght@0,300;0,400;0,600;0,700;1,400;1,700
    - https://cdn.jsdelivr.net/npm/lxgw-wenkai-webfont@1.1.0/style.css
    - https://cdn.jsdelivr.net/npm/lxgw-wenkai-screen-webfont@1.1.0/style.css
    - style.css
plugins:
    - echarts

<slide :class="aligncenter size-70">
<link rel="stylesheet" href="style.css">

# Python 基础教学 {.text-shadow}

---

By @鹤翔万里（TonyCrane） {.text-intro}

[:fa-github: Github](https://github.com/ksky521/nodeppt){.button.ghost}

<slide :class="size-60">

# 前言

---

- 这次的教学面向没有学过 python 的人，不论有没有编程基础都可以听懂
- 这里说的东西有些只是为了更好的理解，可能并不严谨，请不要完全听信（~~免责声明~~
{.description}

<slide :class="size-60">

# 为什么讲 python

---

- **manim 动画引擎的基础**{.tobuild.fadeInUp}

&emsp;&emsp;manim 是用 python 编写的库，使用需要有 python 的基础知识（~~不然会被我劝退.jpg~~）{.tobuild.fadeInUp}

- **易用易学、作为工具**{.tobuild.fadeInUp}

&emsp;&emsp;python 这个语言很易学，特别是对于有编程基础的人（几乎直接上手）。所以有些教程、课程其实过于冗余{.tobuild.fadeInUp}

- **大学某些课程、老师会默认你会**{.tobuild.fadeInUp}

<slide :class="size-60">

# 什么是 python

---

::: shadowbox

## &nbsp;解释性的脚本语言

&nbsp;&nbsp;通过解释器来直接运行，不需要编译链接成二进制文件

---

## &nbsp;动态类型语言

&nbsp;&nbsp;类型在运行时确定，不需要通过代码明文规定

---

## &nbsp;面向对象语言

&nbsp;&nbsp;python 中一切皆对象

---

## &nbsp;...

:::

<slide :class="size-60">

# 怎么装 python

---

- **装的是什么？**{.tobuild.pulse}
    - 是一个 python *解释器*，以及运行需要的*环境*{.tobuild.fadeInUp}
- **怎么装？**{.tobuild.pulse}
    - 官方网站 [https\://www.python.org/downloads/](https://www.python.org/downloads/)
    {.tobuild.fadeInUp}
    - conda（一个好用的 python 环境管理工具）{.tobuild.fadeInUp}
        - anaconda （大、有预装环境）[https://www.anaconda.com/](https://www.anaconda.com/)
        {.tobuild.fadeInUp}
        - miniconda （小）[https://docs.conda.io/en/latest/miniconda](https://docs.conda.io/en/latest/miniconda.html)
        {.tobuild.fadeInUp}
    - **极不建议通过微软应用商店安装 python**{.tobuild.fadeInUp}
- **装什么版本？**{.tobuild.pulse}
    - 两个大版本，2.\* 和 3.\*，差别较大，建议 3.\*{.tobuild.fadeInUp}
    - 一些小版本，3.6 及之前不推荐，3.7 3.8 稳定，3.9 3.10 完善中，3.11 预览中{.tobuild.fadeInUp}
    - 细分版本，选择最新，3.7.13、3.8.13、3.9.12、3.10.4{.tobuild.fadeInUp}
    - conda 不必担心版本，默认 3.9，可以通过创建虚拟环境来使用不同版本{.tobuild.fadeInUp}

<slide :class="size-60">

# 怎么编写、运行 python

---

- **怎么用 python？**{.tobuild.pulse}
    - 记住你下载的是一个解释器，建议通过命令行运行 python code.py{.tobuild.fadeInUp}
- **什么是命令行？**{.tobuild.pulse}
    - 通过输入命令来通知电脑执行某指令、或者运行某程序{.tobuild.fadeInUp}
    - Windows：cmd、Powershell -> 单独运行 / **Windows Terminal** /...{.tobuild.fadeIn}
    - macOS：zsh、... -> 终端 / iTerm /...{.tobuild.fadeIn}
    - Linux：bash、zsh、... -> 终端 / ...{.tobuild.fadeIn}
- **用什么写代码？**{.tobuild.pulse}
    - 记住你编写的只是一个 .py 作为扩展名的文本文件 ~~只要文本编辑器都可以写~~{.tobuild.fadeInUp}
    - ~~记事本、自带 IDLE、word~~{.fadeIn}
    - Notepad++、Sublime Text{.fadeIn}
    - VSCode（Visual Studio Code，不是 VS）[code.visualstudio.com](https://code.visualstudio.com/){.fadeInUp}
    - Pycharm（Community Edition 就够用）[jetbrains.com/pycharm](https://www.jetbrains.com/pycharm/){.fadeInUp}
    {.build}

<slide :class="size-60">

# Hello world!

---

```python
print("Hello world!")
```

<slide :class="size-60">

# 变量

---

- 给一个内容绑定一个标签即变量名（注意请不要认为变量类似一个“盒子”）{.tobuild.pulse}
- 通过 = 来定义变量，变量名 = 内容{.tobuild.pulse}
- 动态类型，不需要规定类型（可以通过 `变量名: 类型 = 内容` 来进行类型标注）{.tobuild.pulse}
- 变量名{.tobuild.pulse}
    - 只能包含字母、数字、下划线、~~中文~~，不能有空格和其它符号{.tobuild.fadeInUp}
    - 只能以字母、下划线开头，不能以数字开头，而且大小写敏感{.tobuild.fadeInUp}
    - 不能用关键字（例如 if def 等）作为变量名，不推荐使用内置函数名作为变量名{.tobuild.fadeInUp}
    - 清晰明确、风格统一{.tobuild.fadeInUp}
    - 全大写一般表示常量、不建议使用双下划线开头或者开头结尾、不建议使用 _ 作为变量名{.tobuild.fadeInUp}

<slide :class="size-60">

# 数字与运算

---

- 1 是整数，1. 是浮点数{.tobuild.pulse}
- 整数与浮点数转换{.tobuild.pulse}
    - int(...)：向 0 舍入{.tobuild.fadeInUp}
    - round(...)：修约（四舍六入五凑偶，可以当成四舍五入）{.tobuild.fadeInUp}
    - math.floor(...)、math.ceil(...)：下取整、上取整（需要 import math）{.tobuild.fadeInUp}
- 运算{.tobuild.pulse}
    - \+ \- \* 加减乘，左右都是整数结果也是整数，有浮点数结果就是浮点数{.tobuild.fadeInUp}
    - / 除法，结果是浮点数（即使可以整除）{.tobuild.fadeInUp}
    - // 整除，结果是整数，向下取整{.tobuild.fadeInUp}
    - % 取模，a % b == a - (a//b)*b（和 c 的行为不一致）{.tobuild.fadeInUp}
    - \*\* 乘方，可以是浮点数，比如 a \*\* 0.5 表示开根号{.tobuild.fadeInUp}
    - pow(a, b, mod)：也是乘方，mod 可以省略，如果有 mod 则对结果取模，如果 mod 为 -1 则计算乘法逆元{.tobuild.fadeInUp}
    - 更多运算通过 math、numpy、scipy 等包来进行{.tobuild.fadeInUp}

