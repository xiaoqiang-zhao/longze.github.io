# Mac 的使用技巧

> 从 Windows 切换到 Mac 在操作上总有一些不一样，这里记录一下使用过程中的一些技巧。

## 通用快捷键

- 在所有开启程序间跳转 Com + Tab
- 打开新窗口 Com + N (特别适用于打开新的 Finder 、 命令行 、QQ) 
- 全屏窗口/退出全屏 Ctrl + Com + F (对QQ无效)
- 最小化当前窗口 Com + M
- 关闭当前窗口 Com + W   (对于浏览器是关闭当前Tab页的意思)
- 退出程序 Com + Q (对于 Finder 这样的系统程序无效)

## chrome 浏览器快捷键

- 打开收藏夹 Option + Com + B
- 隐藏/显示收藏夹 Shift + Com + B
- 打开历史记录 Com + Y
- 打开新标签页 Com + T
- 打开新窗口 Com + N (与其他程序相同)
- 进入隐身模式 Shift + Com + N
- 全屏窗口/退出全屏 Com + Ctrl + F
- 隐藏和展示全部的工具栏 Com + Shift + F
- 光标到地址栏 Com + L
- 向左右切换页面 Option + Com + 左右方向键
- 开发调试时的F8、F10、F11功能键的使用需要单独设置，勾选 “系统偏好设置/键盘/将F1、F2等键用作标准功能键”

注：Chrome默认情况下是不支持修改快捷键的，但是可以安装插件的方式来支持，推荐插件“Keyconfig”。

## 锁屏

> 在公司办公人离开电脑把电脑锁屏是必要的，大公司特别注意这一点，甚至IBM的制度中有离开电脑不锁屏可以开除的规定，锁屏绝对是个好习惯，尤其是对于启动速度超快的Mac。

- 休眠 Ctrl + Shift + 电源键，Mac 上没有锁屏的概念，锁屏通过休眠和设置休眠后启动需要输入密码来实现，后者可以在 “系统偏好设置/安全与隐私/通用/进入睡眠或开始屏保程序立即要求输入密码” 下设置

## 新建txt文件

【Launchpad 程序选择(一般三指抓合)/其他/文本编辑器/新建文稿/格式/制作纯文本】写内容然后保存就可以

## One App One Key Map

> 一个应用，一个常用的快捷键

- 在Finder的任何位置，选中这里所有的图片，进入全屏幻灯片模式 Com + Option + Y 
- QQ 的Swiftly，当你想搜一个东西的时候不需要去找浏览器，然后打开百度，最后输入你想找的东西；敲两下 Com 键直接搜索。QQ默认的搜索引擎是Google，可以在QQ的偏好设置下设置默认搜索引擎和输入法

## 配置

- F1 到 F12 是功能键，默认状态下只有按着左下角的fn键才是原始功能，如果想倒过来需勾选 “系统偏好设置/键盘/将F1、F2等键用作标准功能键”

- 快速找到并启动程序：Cmd + Space，这需要在 System Preferences/Keyboard/Shortcuts 下 将 Spotlight 选中，如果搜索出现卡顿可以在 System Preferences/Spotlight 中配置检索项，减少需要检索的内容会提升速度。

## 命令行

- 回到上一级目录 cd .. (注意 cd 后面要跟一个空格，和windows的不同；另外有一个插件Go2Shell可以让你从Finder中直接进入当前目录命令行，在appStore中就可以找到)
- 查看当前目录下的文件 ls (加 “空格-a” 可现实隐藏文件)
- 查看当前目录下的文件并且包含文件的详细信息 ll (加 “空格-a” 可现实隐藏文件)
- pwd 查看当前路径
- open + space + 文件名 打开文件
- Tab 键自动补齐
- 删除文件 rm filename
- 删除文件夹 rmdir dirname
- 修改文件名 
- 清屏 Com + K
- sudo chmod og+w /etc/hosts 配置 hosts 编辑权限

## host 的配置

这里用到了 vim 的操作技巧，着实为难了一下，但那已成为过去。

打开命令行输入 `sudo vi /etc/hosts` 然后回车

会提示让你输入密码（注意输入密码时你看不到＊号）

输入成功以后，出现的界面让你选操作方式，下键调出选项并再按e，转入编辑模式

键入 i 或者 a 或者 o，才可进行编辑

输入你要设定的hosts内容，比如：127.0.0.1 tw.dev.map.yahoo.com，注意你输入的字符在选中字符的前面

输入完毕，如果要保存退出，按 esc，再输入 `:wq!`，再按回车，hosts就保存生效了

为了避免错误，最好是再清除一次浏览器的cache。

FireFox 的 HostAdmin 插件很好用，可以方便的切换 host 配置。

工具：switchHosts、HostsAdmin、Chrome插件Host Switch Plus。

## 显示隐藏文件

- 按快捷键Command + F 调出搜索窗口
- 点击"种类"选项卡,在下面找到"其他"
- 在弹出的窗口里 找到"文件不可见性" 选项(可通过搜索快速查找),不勾选后面的方框,点击"好"保存设置

## 软件推荐

- Dash 长按 Command 键出现当前软件的快捷键；
- [BetterZip](https://macitbetter.com/)，Mac 下的免费压缩和解压工具；
- [Kap](https://getkap.co/)，录屏生成 gif 软件； 
- [CleanMyMac](https://macpaw.com/cleanmymac)，Mac 上的垃圾清理工具和软件管理工具(收费)。

## 开发工具推荐

- ZSH 终端神器，[传送门](http://blog.163.com/qy_gong/blog/static/1718738792013102992830558/)；
- 前端神器 WebStorm，参见另一篇文章 [WebStorm 使用文档](/index.html#!/articles/webstorm)
- 代理工具 [Charles](https://www.charlesproxy.com/)
- 高效的设计稿标注、测量工具 [MarkMan](http://www.getmarkman.com/)
- 发送网页HTTP请求的工具，请求[Postman](https://www.getpostman.com/apps)

## 外接显示器

外接显示器分辨率没有最佳分辨率选项，需要按住 option 键再点击缩放按钮，这样会列出所有的分辨率选项。

## 资料

[16个OS X快捷键小技巧，至少应该了解一半](http://www.macx.cn/thread-2050934-1-1.html)
