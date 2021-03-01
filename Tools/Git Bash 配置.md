### 1.配色主题设置
在用户目录创建.minttyrc文件：`vim ~/.minttyrc`
配置文件设置如下：
```
BoldAsFont=yes
FontHeight=12
Scrollbar=none
Term=xterm-256color
BoldAsColour=yes
Black=7,54,66
Red=220,50,47
Green=133,153,0
Yellow=181,137,0
Blue=38,139,210
Magenta=211,54,130
Cyan=42,161,152
White=238,232,213
BoldBlack=0,43,54
BoldRed=203,75,22
BoldGreen=88,110,117
BoldYellow=101,123,131
BoldBlue=131,148,150
BoldMagenta=108,113,196
BoldCyan=147,161,161
BoldWhite=253,246,227
ForegroundColour=192,192,192
BackgroundColour=0,43,54
CursorColour=133,153,0
Columns=80
Rows=25

BoldAsFont=-1
Locale=zh_CN
Charset=UTF-8
Font=Consolas
Transparency=off
CursorType=block
CursorBlinks=yes

```
### 2.修改前缀（隐藏用户@主机）
用户目录下添加配置文件`vim ~/.bash_profile`
```
# Shows Git branch name in prompt.
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
# Show User @ Name (still with git branch name)
# export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "
# Or hide User @ Name (still with git branch name)
export PS1="\W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "

```