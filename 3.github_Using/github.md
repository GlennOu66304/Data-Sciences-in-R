# github

## Github search:
```
betterscroll extension:vue
```

[How to search for code in Github](https://www.youtube.com/watch?v=K4FatbcgPIU).  


## Download the certain folder of the github repo:
svn can not be used in MacOS Big Sur 11.0.1 (20B29).:
```
brew install svn
```
[svn can not be used in MacOS Big Sur 11.0.1 (20B29).](https://developer.apple.com/forums/thread/666689)   


1.install the svn:  
```
wget http://opensource.wandisco.com/1.11/scripts/subversion_installer_1.11.sh
chmod +x subversion_installer_1.11.sh

sudo apt-get remove libapache2-svn
sudo apt-get remove libapache2-mod-svn
svn --version
```
[how do I install latest version of svn](https://askubuntu.com/questions/1114618/how-do-i-install-latest-version-of-svn)   

2.replace the tree master with trunk to download the file
```
svn export https://github.com/janosgyerik/jquery-upvote/trunk/lib jquery-upvote-lib

# svn checkout 
svn checkout "https://github.com/xamarin/xamarin-forms-samples/tree/master/Todo"

```
[How to download a project subdirectory from GitHub](https://coderwall.com/p/o2fasg/how-to-download-a-project-subdirectory-from-github)  
[How to download a single folder of a github repository](https://ourcodeworld.com/articles/read/123/how-to-download-a-single-folder-of-a-github-repository)  

### Reference:
[SVN](https://tortoisesvn.net/downloads.html)  
[Git: Download a Repository’s Specific Subfolder](https://medium.com/@marcoscannabrava/git-download-a-repositorys-specific-subfolder-ceeabc6023e2)  
