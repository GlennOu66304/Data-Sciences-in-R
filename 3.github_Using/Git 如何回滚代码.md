> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [zhuanlan.zhihu.com](https://zhuanlan.zhihu.com/p/137856034)

> 这个是Git学习的第5篇内容，今天我们来讲讲Git如何做代码回滚。 代码回滚不知道大家在平常开发时中没有犯过这样一个错误，就是把IDE的配置或者项目运行的本地配置文件上传到服务器，导致别人更新代码之后，出现本…

> IDE 的配置或者项目运行的本地配置文件上
> 
> 备注：  
> Local configuration sync to the server

> 别人更新代码之后，出现本地项目无法运行
> 
> 备注：  
> Other user update the code, then local code can not run

> 出现了紧急 Bug，一时半会无法修复，为了保证线上稳
> 
> 备注：  
> Code return to the original version

> ```
> 使用git log命令，查看分支提交历史，确认需要回退的版本
> 使用git reset --hard commit_id命令，进行版本回退
> 使用git push origin命令，推送至远程分支
> ```
> 
> 备注：  
> git log find the hash id  
> git reset --hard commit_id to go back to the previous version  
> git push origin push to the server

> ```
> 回退上个版本：git reset --hard HEAD^
> ```
> 
> 备注：  
> git reset -- hard Head^ Previous version

> 我们可以用 git checkout -- file 命令，来清空工作区的修改
> 
> 备注：  
> git checkout -file

> 如果想要撤销提交到暂存区后的文件内容怎么办呢
> 
> 备注：  
> recall the git add option

> 使用 git reset HEAD file 命令撤销提交到暂存区的内容
> 
> 备注：  
> git reset HEAD file recall the git add option

> 再使用 git checkout -- file 命令来撤销工作区的修改
> 
> 备注：  
> git checkout --file finish the recall

> reset 是用来 "回退" 版本，而 revert 是用来 "还原" 某次或者某几次提交。

> 在确认要回滚的版本之后，如果别人没有最新提交，那么就可以直接用 reset 命令进行版本回退，否则，就可以考虑使用 revert 命令进行还原修改，不能影响到别人的提交。
> 
> 备注：  
> When to use the reset and revert

> 那如果发现第三次修改有错误，想要恢复第三次修改，却要保留第四次修改呢？
> 
```
git
git revert -n 97ea0f9
git commit -m "恢复第三次修改"
"恢复第三次修改"
```
> 备注：  
> 
> git revert will change the mistake commit content and keep all commit history

> 使用 reset 命令，Git 会把要回退版本之后提交的修改都删除掉。要从第四次修改回退到第一次修改，那么会删除第二、三、四次的修改
> 
> 备注：  
> git reset will change the mistake commit content,and delete the commit after this commit