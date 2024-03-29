# For Mac OS X Macvim

```
cd ~/git && git clone https://github.com/hi20160616/vim.git
ln -s ~/Git/vim/UltiSnips ~/.vim/UltiSnips
ln -s ~/Git/vim/vimrc/vimrc_osx ~/.vim/vimrc
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

# For Linux Neovim

```
cd ~/Git && git clone https://github.com/hi20160616/vim.git
mkdir ~/.config/nvim
ln -s ~/Git/vim/vimrc/init.vim ~/.config/nvim/init.vim
ln -s ~/Git/vim/UltiSnips ~/.vim/UltiSnips
```


# For Windows

Get repository:

```
git clone https://github.com/hi20160616/vim.git
```

# Supplement

## about vimspector

```
ln -s ~/Git/vim/.vimspector.json ~/.vimspector.json
~/.vim/plugged/vimspector/install_gadget.py --enable-<language>
```

## get snippet

go:

https://raw.githubusercontent.com/fatih/vim-go/master/gosnippets/UltiSnips/go.snippets


Repository to settings:

```
cd vim
copy vimrc\gvimrc_windows ~\vimfiles\gvimrc
copy vimrc\vimrc_windows ~\vimfiles\vimrc
robocopy colors ~\vimfiles\colors *
```



Settings to repository:

```
cd vim
copy ~\vimfiles\gvimrc vimrc\gvimrc_windows
copy ~\vimfiles\vimrc vimrc\vimrc_windows
robocopy ~\vimfiles\colors colors *
```



# Experience



YCM 实际上最难安装的插件, 我最近在 Mac Windows Linux 上都搭建使用安装过并且成功运行 C/C++ Go 的功能, 体验到了一些 **过坑哲学** :

1. 如果你发现别人都是好的, 只有你出问题了, 那么考虑更换你的环境. 比如, 如果你要测试这款插件, 你怎么测? 从官网下载 python 安装, 或者最传统的 apt yum brew 的方式去安装, 不用什么版本控制软件.
2. 沿用这个思路以及我们常说的重启大法好的说法, 如果你不是一定要找出插件安装的问题在哪里, 最简单的办法, 减少错误可能发生的条件: 排除其他你的个性安装方式或者其他独特安装办法.
3. 重装大法好, 如果不是要帮助提交代码解决问题, 重装 Vim 或插件也是不错的选择, 至少这可以缩小问题域.
4. Vim 和 YCM 在 Python 编译时路径存在问题, 你通过某种方式管理多版本 Python 可能会让你遇到别人遇不到的问题 , 意味着, 你可能需要手动指定 `python37.dll` 或重装 python 可以解决一些问题.
5. 经过最近一段时间的折腾, 对于 vim 类型选择我是这么理解的:
   1. Macvim 最好用, 所以苹果系统最好用, 电脑最好用. 苹果的确好用, 好稳, 好稳 !!!
   2. Gvim better than Neovim on Windows, 真的如此, 至少 Neovim 打开就是比 Gvim 慢 2020年2月23日我这么说的, 近期应该没什么变化了.
   3.  Neovim's fell good on Linux, you're worth it!


coc-nvim 还是很推荐的，确实如其作者大大所说，给人以vscode一般的体验

内置的CocList 提供一些模糊查找路径，大纲，符号表等 取代了 fzf等同类插件；

coc-explorer 取代了 NERDTree，defx；

coc-pairs 取代了 autopairs；

coc-smartf 取代了 vim-easymotion；

coc-highlight 取代了 vim-cursorline，并提供了颜色板功能（不知道怎么描述，就是可以像ide一样在描述颜色的地方弹出调色窗口

coc-java/ccls/python/rls 取代了那堆各有缺点的补全插件，

coc-pyright 提供 python 静态类型检查,
……
配置也没那么复杂，引入新的配置文件 全局/局部coc-settings.json,就像vscode那样，安装coc-json后提供完整的设置模糊补全，

而这些插件只需要在ex中 :CocInstall 插件名 即可

你甚至可以安装 coc-marketplace 搜索安装更多插件
