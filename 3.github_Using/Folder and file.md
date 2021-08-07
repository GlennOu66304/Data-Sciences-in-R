## 1. Folder and File 


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

## Help, I keep getting a 'Permission Denied (publickey)' error when I push!"
[Help, I keep getting a 'Permission Denied (publickey)' error when I push!"](https://gist.github.com/adamjohnson/5682757). 
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

### 2.Github desk change:
#### If you wan to change the fold name or pdf upload name, you need to do it on the Github desk version.
Change a Git hub a directory's name, a top fold has few small folds. in this situation you can choose the git or github desk:

#### github desk:
1.download the github desk;
<br>GitHub Desktop
<br>https://desktop.github.com/
<br>2. clone the repository into local;
<br>3. change the flod's name in local;
<br>4. Commit this change in the github desk;
<br>5.Fetch the change into github;

#### 3. Creating new folders in GitHub repository via the browser. 
https://github.com/KirstieJane/STEMMRoleModels/wiki/Creating-new-folders-in-GitHub-repository-via-the-browser
#### 4. Can not add a fold before a pdf file by using the solution above. This PDF file was uploaded from computer local.
 in order to prevent this happen, you need to change it by git or using github desk version. 
![picture alt](https://github.com/GlennOu66304/R-Cheat-Sheet/blob/R-Learninh/image/PDF%20file.png)

Moving and Renaming Files on GitHub
<br>https://github.blog/2013-03-15-moving-and-renaming-files-on-github/

### Organize the Data Sciences Guide map  and Single Fold downloading from github.
1.Organize the Data Sciences Guide map with content information(contain the Project Link, Utilize the content information as 
path refer) plus Project Fold format. within Fold contains Code file, Technician Explanation. Please note that you need to build an repository if the project is bigger enough.
You can download the single file from GitHub by using the GitZip:

1.Get Token:
get-token-step.md
<br>https://github.com/KinoLien/gitzip/blob/gh-pages/get-token-step.md

2.inout the token and GitHub single fold URL, Then download it as a ZIP format.
<br>http://kinolien.github.io/gitzip/

3.Answer refer:
<br>1.Download a single folder or directory from a GitHub repo
<br>https://stackoverflow.com/questions/7106012/download-a-single-folder-or-directory-from-a-github-repo
<br>2.How can I download a specific folder from a GitHub repo?
<br>https://github.community/t5/How-to-use-Git-and-GitHub/How-can-I-download-a-specific-folder-from-a-GitHub-repo/td-p/88

4. Project Sample:
<br>https://github.com/GlennOu66304/ViaX-Data-Science-And-Big-Data/tree/master/Week1/Week_1_Glenn-1908_DS80

### Single Fold downlasing, you copuld click that file then go to file details page to choose downlaod option to download it.

## 2. Git ##

Git install:
```
$ git --version 
```
Cloning an Existing Repository
```
$ git clone https://github.com/libgit2/libgit2 mylibgit
```
view all of your settings and where they are coming from using:
```
$ git config --list --show-origin
```
set your user name and email address
```
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
```
Set Your Editor
```
$ git config --global core.editor emacs
```
Checking Your Settings
```
$ git config --list
```
check what Git thinks a specific key’s value is by typing git config key:
 ```
 $ git config user.name
```
Installing on macOS
<br>https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
<br>Change a directory name in a Github repository remotely, directly from local Linux Git?
<br>https://unix.stackexchange.com/questions/424130/change-a-directory-name-in-a-github-repository-remotely-directly-from-local-lin

** Pro Git
<br>https://git-scm.com/book/en/v2
<br>**nnja advanced-git**
<br>https://github.com/nnja/advanced-git/blob/master/presentation/slides.pdf
<br>Git 手冊
<br> https://vincentliu99999.github.io/git-handbook/

### 2.Visul Studio Code
#### Selecting the Color Theme
In VS Code, open the Color Theme picker with **File > Preferences > Color Theme. (Code > Preferences > Color Theme on macOS)**.
<br>Color Themes
<br>https://code.visualstudio.com/docs/getstarted/themes
