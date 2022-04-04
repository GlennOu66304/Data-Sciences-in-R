> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [stackoverflow.com](https://stackoverflow.com/questions/30893040/git-remove-commit-from-history)

> I did something extremely stupid. I entered a curseword in my code and I pushed the code on the master branch. I pushed a few more times after that so people do not pull the bad stuff, but I can st...

> This works for me:
> 
> 1.  `git log` to find the commit you want to remove and copy its hash
> 2.  `git rebase -i <commit_hash>~` which opens your text editor
> 3.  in text editor, switch from `pick` to `drop` for your particular commit:
> 
go to the vim editor, then press i to the editing mode, then choose the drop
and esc, then :x save the change

You can only delete the non header commit history, also commit id choose the bottom one, not first one