###
---
title: 文章标题
date: 创建日期
updated: 更新日期
cover: 文章封面
description: 文章描述
swiper_index: 1 #置顶轮播图顺序，非负整数，数字越大越靠前
---

域名：angus.love
主机记录：alidnscheck
记录值：f6cf3b93a0d147aeaad21fc91c3243a1
#

Git 全局设置:

git config --global user.name "angus"
git config --global user.email "angus9823@163.com"

创建 git 仓库:

mkdir blog-version-controller-for-apan
cd blog-version-controller-for-apan
git init 
touch READMEbyRepo.md
git add README.md     @@@@@@@ git add .
git commit -m "first commit"
git remote add origin https://gitee.com/silenceyb/blog-version-controller-for-apan.git
git push -u origin "master"

已有仓库?

cd existing_git_repo
git remote add origin https://gitee.com/silenceyb/blog-version-controller-for-apan.git
git push -u origin "master"


###