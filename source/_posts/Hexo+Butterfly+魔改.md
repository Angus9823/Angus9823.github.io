---
abbrlink: '0'
---

<!-- title: Hexo_Butterfly+魔改
abbrlink: 201345
date: 2023-03-20 18:19:03
updated: 2023-10-23 22:00:00

description: 🥧本文汇总Markdown格式以及外挂标签在网页端的渲染效果，可作为文档进行查询
mathjax: true
tags:
  - Markdown
  - 外挂标签
categories:
  - 演示
abbrlink: 2013454d
sticky: 2
swiper_index: 2 -->



博客搭建 请参考保姆级系列教程:
【Hexo 从零开始搭建个人博客系列】
https://tzy1997.com/articles/hexo1600/
2、博客搭建过程中遇到任何问题，请优先在站内搜索，检查是否已经有该配置教程。可阅读 【常见问题】 这一篇文章:
https://tzy1997.com/articles/hexo1612/
3、系列视频教程:
https://space.bilibili.com/220757832
4、若是遇到无法解决的bug，可以@群主或者管理，记得配上错误截图。

# Hexo博客搭建基础教程(一)

**前言📝**

这部分教程有参考tzy大佬的文章：[基于 Hexo 从零开始搭建个人博客（一）](https://tzy1997.com/articles/hexo1601/)、[基于 Hexo 从零开始搭建个人博客（二）](https://tzy1997.com/articles/hexo1602/)
全程我将会用一个完全空白的虚拟机带着大家进行搭建，大家可以放心食用🍖🍖🍖
视频教程会同步至在我的B站账号[**–Fomalhaut**](https://space.bilibili.com/220757832)

**博客搭建与魔改系列教程导航🚥🚥🚥**

1. [🥬Hexo博客搭建基础教程(一)](https://www.fomal.cc/posts/e593433d.html) ⇦当前位置🪂
2. [🍒Hexo博客搭建基础教程(二)](https://www.fomal.cc/posts/4aa2d85f.html)
3. [🥪Hexo博客搭建基础教程(三)](https://www.fomal.cc/posts/3451f874.html)
4. [🍀博客魔改教程总结(一)](https://www.fomal.cc/posts/eec9786.html)
5. [🍚博客魔改教程总结(二)](https://www.fomal.cc/posts/5389e93f.html)
6. [🎋博客魔改教程总结(三)](https://www.fomal.cc/posts/2d7ac914.html)
7. [🥕博客魔改教程总结(四)](https://www.fomal.cc/posts/d739261b.html)
8. [🍊博客魔改教程总结(五)](https://www.fomal.cc/posts/d1927166.html)
9. [🧄博客魔改教程总结(六)](https://www.fomal.cc/posts/489d3914.html)
10. [🎨综合美化模块教程](https://www.fomal.cc/posts/9ac969bb.html)

## 1.前言

1. 博客搭建过程遇到任何问题，优先在本页面搜索，检查是否已经有该配置教程。
2. 遇到问题可以优先在文章评论区留言，注意留言时请填写正确的邮箱以确保能收到站长的回复。
3. 实在解决不了的问题可添加站长的微信进行交流，备注自己的个人信息。

## 2.环境与工具准备

**本教程主要面对的是Windows用户**

- 操作系统：Windows10
- Node
- Git
- Hexo
- 文本编辑器(强烈推荐VSCODE)
- GitHub 帐号
- 一个域名（强烈推荐买个域名）
- 云服务器（可选）

## 3.Node的安装

1. 打开Node官网，下载和自己系统相配的Node的安装程序，否则会出现安装问题。下载地址：https://nodejs.org/en/download/
   我个人的版本是 12.19.0，目前版本已经更新到19.0.0，按照个人经验，可以选个低一些的版本，可以和我的一样，否则后面会出现各种不兼容的问题！我之前就是安装16的，系统无法识别，如果大家遇到问题建议选个低版本的！历史版本下载页面：https://nodejs.org/en/download/releases/
   [![image-20221027173738226](Hexo+Butterfly+魔改.assets/876780920daf4f8fb319d49ff68f17a3)](https://s1.vika.cn/space/2022/10/27/876780920daf4f8fb319d49ff68f17a3)

2. 下载后安装，安装的目录可以使用默认目录【C:/Program Files/nodejs/】，也可以自定义路径。
   这个环境路径切换坑也很多，如果大家C盘空间足够可以直接装C盘，如果想切换其他盘或者把环境遍历切换到自定义路径也可以，具体教程百度(不过坑比较多就是了)!

3. 安装完成后，检查是否安装成功。在键盘按下win + R键，输入CMD，然后回车，打开CMD窗口，执行node -v命令，看到版本信息，则说明安装成功。

4. 修改npm源。npm下载各种模块，默认是从国处服务器下载，速度较慢，建议配置成淘宝镜像。打开CMD窗口，运行如下命令:

   ```shell
   SHELLnpm config set registry https://registry.npm.taobao.org
   ```

## 4.安装Hexo

1. 在`Git BASH`输入如下命令安装

   ```shell
   SHELLnpm install -g hexo-cli
   ```

2. 安装完后输入hexo -v验证是否安装成功。

[![image-20221027173525181](Hexo+Butterfly+魔改.assets/f05830f48da44ea98d2a55c3a6663004)](https://s1.vika.cn/space/2022/10/27/f05830f48da44ea98d2a55c3a6663004)

## 5.Github注册与创建仓库

1. 进入官网 https://github.com/
   [![Github注册](Hexo+Butterfly+魔改.assets/627d2c0449341.webp)](https://bu.dusays.com/2022/05/12/627d2c0449341.webp)
2. 点击右上角的 Sign up(注册)
   [![Github注册](Hexo+Butterfly+魔改.assets/627d2c05ee628.png)](https://bu.dusays.com/2022/05/12/627d2c05ee628.png)
3. 填写自己的邮箱、密码、用户名等信息，然后用邮箱验证即可完成。
4. 注册完成后，点击右上角的`+`按钮，选择`New repository`，创建一个`<用户名>.github.io`的仓库。

[![image-20221027110619071](Hexo+Butterfly+魔改.assets/7a06143d180d47088833a486732dccf5)](https://s1.vika.cn/space/2022/10/27/7a06143d180d47088833a486732dccf5)

- 仓库的格式必须为：`<用户名>.github.io` (注意：前缀必须为用户名，不要等后面404了再来为什么！！！)
- Description：为描述仓库（选填）
- 勾选 Initialize this repository with a README 初始化一个 [README.md](http://readme.md/) 文件
- 点击 Creat repository 进行创建

[![image-20221027111641909](Hexo+Butterfly+魔改.assets/0a4dbb10ca69422ca9ccb7493d0f177a)](https://s1.vika.cn/space/2022/10/27/0a4dbb10ca69422ca9ccb7493d0f177a)

## 6.Git安装

1. 进入官网：https://git-scm.com/downloads ，由于官网下载太慢可以通过淘宝的开源镜像下载 网址：https://registry.npmmirror.com/binary.html?path=git-for-windows/v2.36.1.windows.1/ ，下载版本更具自己的需求选择即可。

   [![image-20221027111755697](Hexo+Butterfly+魔改.assets/28a7d7e6ef3f4df080da8d7e8337431b)](https://s1.vika.cn/space/2022/10/27/28a7d7e6ef3f4df080da8d7e8337431b)

2. 下载后傻瓜式安装Git即可，安装的目录可以使用默认目录【C:/Program Files/Git】，也可以自定义路径。

3. 点击电脑左下角开始即可看见`Git Bash`。

[![Git Bash](Hexo+Butterfly+魔改.assets/627d410ddc940.webp)](https://bu.dusays.com/2022/05/13/627d410ddc940.webp)

- `Git CMD` 是windows 命令行的指令风格
- `Git Bash` 是linux系统的指令风格（建议使用）
- `Git GUI`是图形化界面（新手学习不建议使用）

1. 常用命令

   ```
   SHELLgit config -l  //查看所有配置git config --system --list //查看系统配置git config --global --list //查看用户（全局）配置
   ```

2. 配置用户名和邮箱

   ```
   SHELLgit config --global user.name "你的用户名"git config --global user.email "你的邮箱"
   ```

3. 通过`git config -l` 检查是否配置成功，至此git安装及配置全部完成。

   [![image-20221027112049822](Hexo+Butterfly+魔改.assets/9115d60b377a47f3a8b79779a287ee65)](https://s1.vika.cn/space/2022/10/27/9115d60b377a47f3a8b79779a287ee65)

## 7.连接至Github

1. 执行以下命令生成ssh公钥，此公钥用于你的计算机连接Github

   ```
   SHELLssh-keygen -t rsa -C "你的邮箱"
   ```

   之后打开C盘下用户文件夹下的.ssh的文件夹，会看到 id_rsa.pub

   [![公钥](Hexo+Butterfly+魔改.assets/627e87126fc59.png)](https://bu.dusays.com/2022/05/14/627e87126fc59.png)

   用记事本打开上述图片中的公钥（id_rsa.pub），复制里面的内容，然后开始在github中配置ssh密钥。

   [![记事本打开公钥](Hexo+Butterfly+魔改.assets/627e87156038a.png)](https://bu.dusays.com/2022/05/14/627e87156038a.png)

2. 将 SSH KEY 配置到 GitHub
   进入github，点击右上角头像 选择`settings`，进入设置页后选择 `SSH and GPG keys`，名字随便起，公钥填到`Key`那一栏。

   ![image-20221027112347632](Hexo+Butterfly+魔改.assets/4a69d999fed54ff78a5b84805d3c6a12)

   [![image-20221027112416710](Hexo+Butterfly+魔改.assets/aa20ae7d8db34e2596638f5f031f0814)](https://s1.vika.cn/space/2022/10/27/aa20ae7d8db34e2596638f5f031f0814)

   [![image-20221027112657256](Hexo+Butterfly+魔改.assets/eaccde8a10eb4cde945a1ed221bb6ace)](https://s1.vika.cn/space/2022/10/27/eaccde8a10eb4cde945a1ed221bb6ace)

3. 测试连接，输入以下命令

   ```
   SHELLssh -T git@github.com
   ```

   [![image-20221027112918539](Hexo+Butterfly+魔改.assets/122bb1ef33074bee84030a525ce1ec56)](https://s1.vika.cn/space/2022/10/27/122bb1ef33074bee84030a525ce1ec56)

   出现连接到账户的信息，说明已经大功告成，至此完成了环境准备工作。

## 8.初始化 Hexo 项目

1. 在目标路径（我这里选的路径为【C:/Hexo-Blog】）打开cmd命令窗口，执行`hexo init`初始化项目。

   ```
   SHELLhexo init blog-demo(项目名)
   ```

   [![image-20221027113206776](Hexo+Butterfly+魔改.assets/1fbeb52671cf4b1daeca3660d1a31a2f)](https://s1.vika.cn/space/2022/10/27/1fbeb52671cf4b1daeca3660d1a31a2f)

2. 进入`blog-demo` ，输入`npm i`安装相关依赖。

   ```
   SHELLcd blog-demo  //进入blog-demo文件夹npm i
   ```

   [![image-20221027113331624](Hexo+Butterfly+魔改.assets/150eeb3e61c94b89a1cad2a3079b1f94)](https://s1.vika.cn/space/2022/10/27/150eeb3e61c94b89a1cad2a3079b1f94)

3. 初始化项目后，`blog-demo`有如下结构：

[![image-20221027113438707](Hexo+Butterfly+魔改.assets/70cf503f27c54d30a31c6b13735023b7)](https://s1.vika.cn/space/2022/10/27/70cf503f27c54d30a31c6b13735023b7)

【node_modules】：依赖包
【scaffolds】：生成文章的一些模板
【source】：用来存放你的文章
【themes】：主题
【.npmignore】：发布时忽略的文件（可忽略）
【_config.landscape.yml】：主题的配置文件
【config.yml】：博客的配置文件
【package.json】：项目名称、描述、版本、运行和开发等信息

1. 输入hexo server或者hexo s 启动项目

   [![image-20221027113534970](Hexo+Butterfly+魔改.assets/688592f6db1448d29a2f722fc7a0bb0a)](https://s1.vika.cn/space/2022/10/27/688592f6db1448d29a2f722fc7a0bb0a)

2. 打开浏览器，输入地址：http://localhost:4000/ ，看到下面的效果，说明你的博客已经构建成功了。

   [![博客首页](Hexo+Butterfly+魔改.assets/628e5423df640.webp)](https://bu.dusays.com/2022/05/26/628e5423df640.webp)

## 9. 将静态博客挂载到 GitHub Pages

1. 安装 hexo-deployer-git

   ```
   SHELLnpm install hexo-deployer-git --save
   ```

2. 修改 _config.yml 文件
   在blog-demo目录下的_config.yml，就是整个Hexo框架的配置文件了。可以在里面修改大部分的配置。详细可参考官方的[配置描述](https://hexo.io/zh-cn/docs/configuration)。
   修改最后一行的配置，将repository修改为你自己的github项目地址即可，还有分支要改为`main`代表主分支（注意缩进）。

   ```
   YAMLdeploy:  type: git  repository: git@github.com:Fomalhaut-Blog/Fomalhaut-Blog.github.io.git  branch: main
   ```

3. 修改好配置后，运行如下命令，将代码部署到 GitHub（Hexo三连）。

   ```
   SHELLhexo clean && hexo generate && hexo deploy  // Git BASH终端hexo clean; hexo generate; hexo deploy  // VSCODE终端
   ```

   - hexo clean：删除之前生成的文件，若未生成过静态文件，可忽略此命令。

   - hexo generate：生成静态文章，可以用`hexo g`缩写

   - hexo deploy：部署文章，可以用`hexo d`缩写

     [![image-20221027113704801](Hexo+Butterfly+魔改.assets/7ed7b8256d75408aa86e90cd37d0ea53)](https://s1.vika.cn/space/2022/10/27/7ed7b8256d75408aa86e90cd37d0ea53)

     注意：deploy时可能要你输入 username 和 password。

     如果出现`Deploy done`，则说明部署成功了。

     [![image-20221027113756069](Hexo+Butterfly+魔改.assets/85b61e7242214d368539d744b4778a5d)](https://s1.vika.cn/space/2022/10/27/85b61e7242214d368539d744b4778a5d)

     稍等两分钟，打开浏览器访问：[https://Fomalhaut-Blog.github.io](https://Fomalhaut-blog.github.io/) ，这时候我们就可以看到博客内容了。

     [![image-20221027113923949](Hexo+Butterfly+魔改.assets/6de50dfe03604b07aa26fb7dd5fe1f99)](https://s1.vika.cn/space/2022/10/27/6de50dfe03604b07aa26fb7dd5fe1f99)

## 10. 无法连接至Github的解决方案

注意：当你在与Github进行ssh通信时候出现超时或者是连接被关闭的情况，可以尝试以下解决方案。

1. 挂代理和换网络（这个就不用多说了）

2. [Git问题：解决“ssh:connect to host github.com port 22: Connection timed out”](https://blog.csdn.net/weixin_41287260/article/details/124368189)

   这是评论区的朋友提供的，可以解决SSH连接超时等问题

3. 开源项目[Github520](https://github.com/521xueweihan/GitHub520)

   通过修改Host文件的方法解决访问速度慢的问题

连接有效性检验：

```
BASH# 任选其一即可ping github.comssh -T git@github.com
```



作者

Fomalhaut🥝

发布于

2022-10-25