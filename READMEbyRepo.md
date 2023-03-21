###
#

Git 全局设置:

git config --global user.name "angus"
git config --global user.email "angus9823@163.com"

创建 git 仓库:

mkdir blog-version-controller-for-apan
cd blog-version-controller-for-apan
git init 
touch READMEbyRepo.md
git add README.md
git commit -m "first commit"
git remote add origin https://gitee.com/silenceyb/blog-version-controller-for-apan.git
git push -u origin "master"

已有仓库?

cd existing_git_repo
git remote add origin https://gitee.com/silenceyb/blog-version-controller-for-apan.git
git push -u origin "master"


###