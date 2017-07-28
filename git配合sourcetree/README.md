# git配合sourceTree演示流程

## 步骤1

新创建一个仓库叫gitdemo，创建一个文件README.md，提交信息为init，如下图

## ![](/git配合sourcetree/assets/DingTalk20170728103336.png)步骤2

git branch -b daily/0.0.1 创建一个分支daily/0.0.1，daily/0.0.1和master共享一个点

![](/git配合sourcetree/assets/DingTalk20170728105024.png)

## 步骤3

修改README.md，产生一个灰色未提交的点

![](/git配合sourcetree/assets/DingTalk20170728105346.png)

## 步骤4

提交本地仓库，提交信息为change readme.md，产生一个新的空心节点\(当前分支所在的节点\)

![](/git配合sourcetree/assets/DingTalk20170728105552.png)

## 步骤5

把master,daily/0.0.1都推到远程仓库，并修改本地daily/0.0.1分支，并提交到本地仓库，提交信息为append string

![](/git配合sourcetree/assets/DingTalk20170728110300.png)

## 步骤6

将daily/0.0.1推送到远程仓库，origin/daily/0.0.1的tag添加到了空心节点

![](/git配合sourcetree/assets/DingTalk20170728110510.png)

## 步骤7

切到master分支，并创建daily/0.0.2分支

![](/git配合sourcetree/assets/DingTalk20170728110730.png)

## 步骤8

修改README.md，并提交修改，提交信息为change in daily/0.0.2，开始出现了分叉

![](/git配合sourcetree/assets/DingTalk20170728111017.png)

## 步骤9

切到daily/0.0.1分支，创建分支daily/0.0.3

![](/git配合sourcetree/assets/DingTalk20170728111622.png)

## 步骤10

修改文件，并提交修改，提交信息你为change in daily/0.0.3

## ![](/git配合sourcetree/assets/DingTalk20170728112352.png)步骤11

切回daily/0.0.1，修改文件，提交修改，提交信息为change after commit daily/0.0.3

![](/git配合sourcetree/assets/DingTalk20170728112604.png)

## 步骤12

切到daily/0.0.2，两次修改和提交，并推送到远程仓库，然后再次修改和提交

![](/git配合sourcetree/assets/DingTalk20170728113253.png)

## 步骤13

切到daily/0.0.3，两次修改和提交，并推送到远程仓库

![](/git配合sourcetree/assets/DingTalk20170728113814.png)

## 步骤14

git merge daily/0.0.1 合并本地daily/0.0.1，并提交merge with daily/0.0.1



## 步骤15



