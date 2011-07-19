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



#下午
#设置vim
    如：vim a.c 在普通模式下
	":set number"         设置显示行号
	":set nonumber"       设置消除行号
    ……
	注此时只能设置 文件 a.c 若想一劳永逸则：
    在用户主目录(即：/home/psjicfh)下面:
	psjicfh@ubuntu:~$ vim .vimrc
	进去后在“插入”模式下设置：
	"set number"         设置显示行号
    ……
    "set tabstop=4"      实际的 tab 即为 4 个空格, 而不是缺省的 8 个
	"set hidden"		 用vim打开一个（或多个）文件后不用保存“w” 亦可bn到下一个						 文件，若不设置则会有警告。
	例如：
	psjicfh@ubuntu:~/work/lesson5$ vim a.c b.c
	在普通模式下“:ls”
		:ls
				  1 %a   "a.c"                          第 1 行
				  2      "b.c"                          第 0 行
					 1 表示打开的文件序号, 这个序号很有用处.
                     %a              表示文件代号, % 表示当前编辑的文件,
                                     # 表示上次编辑的文件
                     "a.c"   表示文件名.
                     行 162          表示光标位置.

	此时先进入a.c中在编辑了a.c后，若想直接bn到b.c中就要设置 “hidden”

	若psjicfh@ubuntu:~/work/lesson5$ vim a.c
    想从a.c跳到b.c中则“:e b.c”
	若此时想要跳到c.c中而此文件在用户主目录下 则：
	psjicfh@ubuntu:~/work/lesson5$ vim a.c
	后要在普通模式下“:e ~/c.c” 就能进入 c.c  然后bn 就可以两个文件间交换编辑
					  “~”代表用户主目录即：“/home/psjicfh”
    进入c.c后就可以编辑了（如：利用可视行进行复制粘贴等） 注意 退出的时候要先 w     后 bd 然后回到a.c中
	注：在两个vim下不能用可视行进行粘贴复制等
    
###更多vim设置请看   http://qinlong.blog.51cto.com/1130504/337730

#设置gitconfig
	
