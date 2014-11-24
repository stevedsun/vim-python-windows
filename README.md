Vim python windows平台开发配置文件
==================


适用于python开发的Vim插件配置，需要gVim版本大于7.4
使用方法

下载全部文件后，复制vim安装目录覆盖同名文件，如果使用rope的定义跳转等功能，需要用pip额外安装python的支持库： （请先确认已经配置好pip后执行下面的操作）

    pip install rope

再进入插件目录vimfiles/bundle/ropevim/下执行:

    python setup.py install


不想使用的插件，可以直接在插件Bundle前边增加"注释掉这行，例如关闭Indent-Guides插件:

    "Bundle 'Indent-Guides'


更换字体，请将_vimrc里的字体设置部分修改为你的字体：

    set guifont=Courier_New:h14

插件说明

    "插件管理器
    Bundle 'gmarik/vundle'
    "状态栏增强
    Bundle 'Lokaltog/vim-powerline'
    "函数名列表
    Bundle 'Tagbar'
    "窗口管理器
    Bundle 'winmanager'
    "markdown语法高亮
    Bundle 'Markdown'
    "文件浏览器
    Bundle 'The-NERD-tree'
    "缓冲区管理器
    Bundle 'bufexplorer.zip'
    "分割线
    Bundle 'Indent-Guides'
    "文件搜索神器
    Bundle 'ctrlp.vim'
    "语法结构补全
    Bundle 'SirVer/ultisnips'
    Bundle 'honza/vim-snippets'
    "字符串自动补全
    Bundle 'AutoComplPop'
    Bundle 'L9'
    "括号补全
    Bundle 'Auto-Pairs'
    "去掉行尾空格,使用:Fixwhitespace
    Bundle 'trailing-whitespace'
    "静态语法检查
    Bundle 'Syntastic'
    "编辑历史记录回滚
    Bundle 'Gundo'
    "python语法检查
    Bundle 'pyflakes.vim'
    Bundle 'pep8'
    "python文档
    Bundle 'pydoc.vim'
    "文档搜索，需要在系统里安装ack-grep
    Bundle 'ack.vim'
    "python补全，跳转，重构(前提pip install rope,ropemode,并且在.vim/bundle/ropevim目录下执行python setup.py install安装)
    Bundle 'ropevim'

快捷键说明

（快捷键可以在.vimrc里通过nmap,vmap,imap后的操作修改）


    fb：打开buffer管理器
    
    fv：横向切分窗口
    
    fs：纵向切分窗口
    
    ft：创建新标签页
    
    fd：关闭当前标签页
  
    ctrl+c：复制选中文件到系统缓冲区
    
    ctrl+v+v：粘贴系统缓冲区内容到当前文本
    
    ctrl+]：跳转到定义处(python ropevim插件)
    
    <F1>：打开文件编辑历史记录(Gundo插件)
    
    <F7>：打开nerd tree文件目录管理器
    
    <F8>：打开tagbar 代码结构管理器
    
    <F9>：创建cscope索引，需要系统中安装cscope
    
    <F10>：创建ctags标签索引，需要系统中安装ctags
    
    ctrl+l/h/j/k:移动光标到右/左/下/上面的窗口
    
    shift+q：关闭其他窗口
    
    alt+q：关闭当前窗口
    
    ctrl+s：启动ack全局搜索
    
    输入模式下xdate回车：插入当前系统时间
