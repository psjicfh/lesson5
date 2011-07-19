#lesson5笔记
##上午
##上传
    git config --global user.name "psjicfh"
    git config --global user.email psjicfh@yeah.net
    git remote add origin git@github.com:psjicfh/lesson5.git
    git push -u origin master

    ctrl+shift+t:同一页面两个标签
    ctrl+pgup(pgdn): 翻页
    用vim打开任何一个文件后会生成一个“.swp”文件
    普通模式下进入可视行：V 后按上下键可选中行
    d:(剪切) y:（复制） p:（粘贴） j:（向上） k:（向下）
    p：（粘贴到当前光标下一行）  P：（粘贴到当前光标处）
    退出可视行模式再按：V
    
    整体缩进几行代码：
    先在可视行模式中选中这几行，然后按“>或<”

#用vim操作多个文件：
    如：vim a.c b.c 即可同时打开两个文件
    在普通模式下 ：ls 即可列出文件
    bn：下一个 bp：上一个 b:buffers（缓存） n:next  p:previous
##例如：
    $: vim a.c  此时想把 a.c 里面的一部分代码写在 b.c 中
    进入可视行模式 剪切要移走的内容
    在普通模式下：“e b.c” 就跳转到 b.c 中
    bn 到 a.c  在bn 到 a.c  w保存 bd关闭一个文件
    普通模式下 ls  只剩一个  
    注：q是 退出 vim


#播放视屏
    wget http://media.happypeter.org/happycasts/happycity/hanzhong-cast/git_branch.ogv

    totem git_branch.ogv

##一次下载多个视屏文件
    wget-r http://media.happypeter.org/happycasts/
