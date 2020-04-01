# Vs Code 常用快捷键

ctrl+p
ctrl+shift+p
ctrl+p 状态下输入<即可切换到 ctrl+shif+p 的状态

## 编辑器与窗口管理

### 同时打开多个窗口

打开一个窗口 ctrl+shift+N
关闭窗口 ctrl+shift+w

### 同时打开多个编辑器

新建文件 ctrl+N
历史打开文件之间进行切换 ctrl+tab,Alt+left,Alt+right
切出一个新的编辑器 ctrl+\
左中右 3 个快捷键的切换方式 ctrl+1,ctrl+2,ctrl+3
编辑器互换位置 ctrl+k 按下之后，按 left 或者 right

## 代码编辑

### 格式调整

代码行缩进 ctrl+[,ctr+]
代码行缩进 Ctrl+[， Ctrl+]
折叠打开代码块 Ctrl+Shift+[， Ctrl+Shift+]
Ctrl+C Ctrl+V 如果不选中，默认复制或剪切一整行
代码格式化：Shift+Alt+F，或 Ctrl+Shift+P 后输入 format code
上下移动一行： Alt+Up 或 Alt+Down
向上向下复制一行： Shift+Alt+Up 或 Shift+Alt+Down
在当前行下边插入一行 Ctrl+Enter
在当前行上方插入一行 Ctrl+Shift+Enter
左侧边栏 打开资源 ctrl+shift+E 打开搜索 ctrl+shift+F 打开 git ctrl+shift+G 打开调试 ctrl+shift+D 打开扩展 ctrl+shift+X 光标相关

移动到行首：Home
移动到行尾：End
移动到文件结尾：Ctrl+End
移动到文件开头：Ctrl+Home
移动到后半个括号 Ctrl+Shift+]
选中当前行 Ctrl+i
选择从光标到行尾 Shift+End
选择从行首到光标处 Shift+Home
删除光标所在行 Ctrl+Delete
Shrink/expand selection（光标所在单词，文档高亮显示相同的）： Shift+Alt+Left 和 Shift+Alt+Right
Multi-Cursor：可以连续选择多处，然后一起修改，Alt+Click 添加 cursor
翻转 IDECtrl+Alt+Down 或 Ctrl+Alt+Up
同时选中所有匹配的 Ctrl+Shift+L
Ctrl+D 下一个匹配的也被选中(被我自定义成删除当前行了，见下边 Ctrl+Shift+K)
回退上一个光标操作 Ctrl+U

### 重构代码

跳转到定义处：F12
定义处缩略图：只看一眼而不跳转过去 Alt+F12
列出所有的引用：Shift+F12
同时修改本文件中所有匹配的：Ctrl+F12
重命名：比如要修改一个方法名，可以选中后按 F2，输入新的名字，回车，会发现所有的文件都修改过了。
跳转到下一个 Error 或 Warning：当有多个错误时可以按 F8 逐个跳转
查看 diff 在 explorer 里选择文件右键 Set file to compare，然后需要对比的文件上右键选择 Compare with 'file_name_you_chose'.

### 查找替换

- 查找 Ctrl+F
- 查找替换 Ctrl+H
- 整个文件夹中查找 Ctrl+Shift+F 匹配符：
- to match one or more characters in a path segment
- ? to match on one character in a path segment
- \*\* to match any number of path segments ,including none
- {} to group conditions (e.g. {\*\*/_.html,\*\*/_.txt} matches all html and txt files)
- [] to declare a range of characters to match (e.g., example.[0-9] to match on example.0,example.1, …

## 显示相关

全屏：F11
zoomIn/zoomOut：Ctrl + =/Ctrl + -
侧边栏显/隐：Ctrl+B
侧边栏 4 大功能显示：
Show Explorer Ctrl+Shift+E
Show SearchCtrl+Shift+F
Show GitCtrl+Shift+G
Show DebugCtrl+Shift+D
输出 Show OutputCtrl+Shift+U
预览 markdownCtrl+Shift+V

## 其他

自动保存：File -> AutoSave ，或者 Ctrl+Shift+P，输入 auto
