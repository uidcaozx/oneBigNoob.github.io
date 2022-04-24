---
title: Git常用命令
date: 2022-04-2 22:55:25
tags: 
---

## 常用命令
```bash
# 设置git的用户名以及邮箱，这和gitee或github的登录账号没有任何关系随便配
git config --global user.name CaoZhixing
git config --global user.email zhixiang_hehe@163.com
# 查看状态
git status
# 将工作区文件添加到暂存区
git add <fielname>
# 将暂存区的文件删除
git rm --cache <fielname>
# 将暂存区文件提交到本地仓库
git commit -m "message" <fielname>
# 查看版本日志信息
git reflog
# 查看版本日志信息（完成的版本号）
git log
# 回到历史版本
git reset --hard <版本号> 
```
## 分支命令
```bash
# 创建分支
git branch <branchname> 
# 查看分支
git branch -v
# 切换分支
git checkout <branchname>
# 将指定分支合并到当前分支
git merge <branchname>
```
## 远程仓库操作
```bash
# 查看当前所有远程地址别名
git remote -v
# 为远程仓库起别名
git remote add 别名 远程地址
# 推送本地分支上的内容到远程仓库
git push 别名 分支名
# 将远程仓库的内容克隆到本地
git clone 远程地址
# 将远程仓库上最新的内容拉下来于对应的本地分支直接合并
git pull 远程仓库地址别名 远程分支名
# 切换远程分支
git remote rm origin
# 添加远程仓库
git remote add origin git@gitee.com:funnymadpee/srb-admin-template.git
# 拉取新仓库的README.md等文件
git pull --rebase origin master
# 查看email
git config user.email
# 生成公钥
ssh-keygen -t rsa -C <email>
# 最新版git一定要注意
ssh-keygen -t ed25519
```
