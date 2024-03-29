# Git Enviroment Build

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

## SourceTree
[Sourcetree在mac平台下的安装与使用超详尽教程](https://www.jianshu.com/p/b8d0547a8449)   
[使用SourceTree](https://www.liaoxuefeng.com/wiki/896043488029600/1317161920364578)  

## Help, I keep getting a 'Permission Denied (publickey)' error when I push!"
[Help, I keep getting a 'Permission Denied (publickey)' error when I push!"](https://gist.github.com/adamjohnson/5682757). 
6.[初次使用git上传代码到github远程仓库](https://zhuanlan.zhihu.com/p/138305054).  

## Set Vs code as your global git editor
[Set Visual Studio Code to be global Git editor on OSX](https://stackoverflow.com/questions/34746045/set-visual-studio-code-to-be-global-git-editor-on-osx)  
## Clone a Private Github Repo
[Github clone with oauth access token](https://stackoverflow.com/questions/42148841/github-clone-with-oauth-access-token)   


## Git uninstall
Git uninstall:[卸载Git](https://blog.csdn.net/weixin_44653603/article/details/87194598)  
Mac系统下安装卸载Git:[Mac系统下安装卸载Git](https://www.jianshu.com/p/898e1516c19a)  

## Git branch delete include locally and remotely
Delete Local Branch
```
$ git branch -d <branch_name>
$ git branch -D <branch_name>
```
[How do I delete a Git branch locally and remotely?](https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-locally-and-remotely)   
