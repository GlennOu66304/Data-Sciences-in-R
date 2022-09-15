

## .env and node_modules stop track
```


git rm .env --cached
git commit -m "Stopped tracking .env File"
```
[git env file ignore](https://github.com/GlennOu66304/ticketsystem-mern)   
## Git rename a branch name
```
git branch -m HEAD newbranch
```
[warning: refname 'HEAD' is ambiguous](https://stackoverflow.com/questions/1692892/warning-refname-head-is-ambiguous)
## Git recall merge command
git reset --hard 
[Git怎样撤销一次分支的合并Merge](https://segmentfault.com/q/1010000000140446)

[Git merge and git rebase](https://www.perforce.com/blog/vcs/git-rebase-vs-git-merge-which-better)   

[git branch merge](https://www.w3schools.com/git/git_branch_merge.asp)   

[Git合并那些事——撤销合并](https://morningspace.github.io/tech/git-merge-stories-5/)   

[Create-react-app - ERROR in Plugin "react" was conflicted between ".eslintrc.json" and "BaseConfig"](https://stackoverflow.com/questions/70449712/create-react-app-error-in-plugin-react-was-conflicted-between-eslintrc-jso/70451413)


branch and github build

(Git)new branch
```
git checkout -b eleme2
```

(Github)new branch push 
```
git push origin eleme2
```

(Git)merge to main branch 
```
git merge main
```

(Git hub)Push to the main branch
```
git push origin main
```
## How to push a local project into the github
```
git init
git add .
git commit -m "CMS"
git branch
git remote add origin git@github.com:GlennOu66304/CMS.git
git branch -M main
git push -u origin main
git branch
```
Remove the origin
```
git remote remove origin
```
[How to remove remote origin from a Git repository](https://stackoverflow.com/questions/16330404/how-to-remove-remote-origin-from-a-git-repository).  

## ! [rejected] master -> master (fetch first)

```
git push origin master --force
```
[! [rejected] master -> master (fetch first)](https://stackoverflow.com/questions/28429819/rejected-master-master-fetch-first) 
```
git pull --rebase origin master
git push origin master
```
[git 解决push报错：! [rejected] master -> master (fetch first) error: failed to push some refs to ' '](https://blog.csdn.net/ourstronger/article/details/103460249?utm_medium=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.no_search_link&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-1.no_search_link)


1.git iniatialize in the project:
```
git init

```
let the local repo from working directory to staging directory
```
git add -A or git add . 
```
[Git: Add All Files to a Repo](https://stackabuse.com/git-add-all-files-to-a-repo).  
then commit it into the final version, it is ready to be placed to the github
```
git commit -m "eleme1"   
```
[工作区和暂存区](https://www.liaoxuefeng.com/wiki/896043488029600/897271968352576).  
2.build the branch:
```
git checkout -b eleme1
```
3.connect with github repo
```
git remote add origin git@github.com:GlennOu66304/Eleme.git 
```
[添加远程库](https://www.liaoxuefeng.com/wiki/896043488029600/900003767775424).  
4.push the branch code to the github
```
git checkout eleme1
git push origin eleme1
```
## Bug fixing:git: updates were rejected because the remote contains work that you do not have locally
```
git branch -a
checkout -b main
git push -f origin main
```
[git: updates were rejected because the remote contains work that you do not have locally](https://stackoverflow.com/questions/24357108/git-updates-were-rejected-because-the-remote-contains-work-that-you-do-not-have).  

## push few files to the github Git
```
git add subway.py
git add subway_beijing.html
git commit -m "subway.py and subway_html"
git branch
 git push origin Quantitative_trading
```
[Saving changes](https://www.atlassian.com/git/tutorials/saving-changes#:~:text=The%20git%20add%20command%20adds,until%20you%20run%20git%20commit%20.).  
## fatal: pathspec 'README.txt' did not match any files
[fatal: pathspec 'README.txt' did not match any files](https://stackoverflow.com/questions/47877925/fatal-pathspec-readme-txt-did-not-match-any-files). 
## Bug:In GitHub, what do I do with “Your recently pushed branches” messages
[In GitHub, what do I do with “Your recently pushed branches” messages](https://www.sitepoint.com/community/t/in-github-what-do-i-do-with-your-recently-pushed-branches-messages/306534).   
### Reference:
1.[廖雪峰Git](https://www.liaoxuefeng.com/wiki/896043488029600/900003767775424).   
2.[deleting branches within your repository](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository).   
3.[5 steps to change GitHub default branch from master to main](https://stevenmortimer.com/5-steps-to-change-github-default-branch-from-master-to-main/).  
4.[尚硅谷】Git与GitHub基础全套完整版教程（快速上手，一套搞定）](https://www.bilibili.com/video/BV1pW411A7a5?p=9).   
5.[万字长文，手把手教你玩转Git！](https://juejin.cn/post/6847902219245715463#heading-36).   
6.[初次使用git上传代码到github远程仓库](https://zhuanlan.zhihu.com/p/138305054).  


### 1.Git file name Change:
```
bogon:~ zt$ cd Data-Sciences-in-R
bogon:Data-Sciences-in-R zt$ git mv README0.md README.md
bogon:Data-Sciences-in-R zt$ git commit -am '[commit messgae]'

[R-Learninh 2d55826] [commit messgae]
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename README0.md => README.md (100%)
 
bogon:Data-Sciences-in-R zt$ git pull

Already up to date.
bogon:Data-Sciences-in-R zt$ git push

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 228 bytes | 228.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/GlennOu66304/Data-Sciences-in-R
   a1d8ba1..2d55826  R-Learninh -> R-Learninh
bogon:Data-Sciences-in-R zt$ 
```
## How do I clone a specific Git branch? [duplicate]
```
git clone -b my-branch git@github.com:user/myproject.git
```

[How do I clone a specific Git branch? ](https://stackoverflow.com/questions/1911109/how-do-i-clone-a-specific-git-branch)

## Git push to github some wrong folder and files
make sure you remove the .git (hiden file CMD + shift + . to check), then git will not track the file
under users directory or desktop.

## List of remotes for a Git repository?
```
git remote -v
```
[List of remotes for a Git repository?](https://stackoverflow.com/questions/10183724/list-of-remotes-for-a-git-repository)   

## Git merge
```
git checkout main
git merge typescript_start
```

> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [www.w3schools.com](https://www.w3schools.com/git/git_branch_merge.asp)

> W3Schools offers free online tutorials, references and exercises in all the major languages of the we......

> ave the emergency fix ready,
> 
> 备注：  
> git sub branch

> merge the master and emergency-fix branches
> 
> 备注：  
> Want to merge the changes in the sub-branch into the main(master) branch

> change to the master branch
> 
> 备注：  
> Go to the main branch first

> merge the current branch (master) with emergency-fix:
> 
> 备注：  
> git merge to the sub-branch: original branch merge to latest branch

[3-way merge](https://www.atlassian.com/git/tutorials/using-branches/git-merge)

