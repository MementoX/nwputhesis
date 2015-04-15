nwputhesis使用方法

# 简介 #

先安装texlive。

在Downloads中下载nwputhesis-bachelor-v1.1.tar.gz，用以下命令解压：
```
tar xvf nwputhesis-bachelor-v1.1.tar.gz
```

进入Bachelor目录中进行编译：

```
make all
```

即可生成main.pdf

如果系统中没有make命令，那么按顺序执行如下命令：
```
xelatex main.tex,
bibtex main.tex,
xelatex main.tex,
xelatex main.tex
```

# 注意事项 #

  * linux和windows下都推荐安装texlive 2011。

  * 将nwpulogo.ttf放到fc-list可以找到的地方。linux下放到~/.fonts，win下放到C:\windows\Fonts。安装完成后执行fc-cache -fv

  * 在setup/format.tex中更改字体，如setCJKmainfont等为你系统中已经安装的字体。

有其它问题请在issue中留言或发我的Email: qy.nwpu at gmail dot com，极力欢迎共同开发:-)。

# 字体问题 #

需要将以下列出的字体装全（怎么装？这可得靠自己机灵了。其实都可以用系统中的字体替换掉），可以用fc-list全部认出，才能通过编译。

尽量避免使用版权字体，大部分采用了开源的字体。

其中不会有版权问题的字体有：

  * TeX Gyre 系列字体: 主要用于替代Times New Roman
  * Latin Modern系列字体: LaTeX自带
  * AR PL UKai TW MBE：楷体，archlinux中的extra中可下到
  * Droid Sans系列字体：google出的，用在Android上的，Apache协议的。
  * nwpulogo：本人自制的毛体“西北工业大学”六个字，版权归老毛同志？

可能有版权问题的字体有：

  * 方正小标宋简体：这个暂时没找到替代的。
  * Adobe Song Std，Adobe Heiti Std：这两个字体的授权我不大明了，哪位懂行的指点一下。实在是找不到矢量的宋体（明体倒是有不少，只是风格和我们看惯的字体不大一样）。