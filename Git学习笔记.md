# Git学习笔记
## Git配置
```bash
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
*注意 “” 前面有空格*

## 在Git上创建版本库
1. 创建空目录
![输入图片说明](/imgs/2026-11-21/hntr6fLmFbNp7iWt.png)
2. 把目录改为版本库
![输入图片说明](/imgs/2026-11-21/jmCkXk7MYHQUW2RR.png)
3. 在版本库中添加文件
![输入图片说明](/imgs/2026-11-21/IjFa8pGoiTLb2Bl7.png)
> 这里一开始我直接添加了文件，但是没有成功，*需要先创建好文件再添加*

> 需要注意add 和commit 两步都不能缺，git add 是放到暂存区，git commit才是存到本地仓库，且git commit 后面要加"- m说明"，否则会出现如下情况![输入图片说明](/imgs/2026-11-21/TqDrQMweTYtFFT06.png)

> 最后可以用git status查看工作区的状态，如果git status显示文件被修改过，还可以用git diff可以查看修改内容

## 用Git Bash发送文件到GitHub仓库
1. 首先需要在GitHub上建立一个仓库（上一阶段已经建好了tasks仓库）
![输入图片说明](/imgs/2026-11-21/Vx98eCPrTUkc5z1O.png)

2. 需要通过链接让Git关联到GitHub上创建的远程库
> 这里我一开始复制的是SSH的链接，但是显示端口网络不通，我又改为http协议的链接，才能够进行发送

![输入图片说明](/imgs/2026-11-21/XoBJ8q9cpR1nb0Rg.png)

> **发送成功之后，我还发现这份文档和我之前在GitHub提交的笔记不在同一分支里**
>这是因为Git软件的本地配置是master且我没有进行提前配置修改
>为避免这个问题，下次可以通过git clone来保证本地和远程一致

## 关于提PR
1. 先Fork 原仓库
![输入图片说明](/imgs/2026-11-21/guJ8Z6HrMUkwFY1I.png)
2. 将学习感想发送到我fork的仓库中
![输入图片说明](/imgs/2026-11-21/6m2PhjZJhS9mR4Zb.png)
3. 最后从网页上完成提pr的操作![输入图片说明](/imgs/2026-11-21/FiGEjnmDWEf3HGKa.png)

## 使用Git Bash的感想
刚开始使用Git Bash需要理清逻辑，查询记忆命令语句确实比较麻烦，相比之下更方便的提交方式有：
- VS Code 源代码管理面板，点按钮就能 add/commit，改动的行的高亮很直观；
- GitHub Desktop，纯图形操作、分支图清晰；
- GitHub 网页直接编辑，零配置改单个小文件

*它们的共同优点是上手快、不用记命令，缺点是都把 Git 底层细节封装起来了，遇到冲突或回滚等复杂情况时就查不出具体问题很难处理*
所以我觉得熟练掌握命令行，只利用图形化工具作为辅助，对于后续学习还是很有必要的。
