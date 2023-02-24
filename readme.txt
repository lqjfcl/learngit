Git is a distribute version control system.
Git is free software

mkdir：创建文件夹
git init：把文件夹变为Git可以管理的仓库
git add：把文件添加到仓库（先在文件夹创建文件）
git commit -m " "：说明提交文件的改动内容，相当于注释
git status：查看仓库当前状态
git diff：查看文件修改内容
git log：显示提交日志（q退出，h查看帮助）
git reset --hard HEAD^：把文件回退到上一个版本
git reflog：查看命令历史
git checkout --file：直接丢弃工作区的修改
情况1：在工作区做了修改，并未添加到暂存区，想撤销工作区的修改，用 git restore file;

情况2：在工作区做了修改，并用git add 添加到了暂存区，未提交；想撤销，分两步，1.先撤销暂存区的修改，用 git restore --staged file, 2.然后参考情况1撤销工作区的修改；

情况3：在工作区做了修改，且git add git commit添加并提交了内容，想撤销本次提交，直接用 git reset --hard HEAD^回退版本，即可保证工作区，暂存区，版本库都是上次的内容
删除文件：rm file
         git rm file        
         git commit -m
    误删可用 git checkout --file 恢复

git push origin master：将本地分支的最新修改推送至GitHub
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

git clone ：从远程库克隆到本地