## 1. Folder and File 
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
