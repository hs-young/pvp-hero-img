# 通过Git工具将本地代码提交到远程仓库
## Git
### 官网
> [https://git-scm.com/](https://git-scm.com/)
### 作用
- 将本地代码提交到远程仓库 → Push
- 从远程仓库拉取代码到本地 → Pull
### 配置
配置用户名和邮箱就行（用户名和邮箱最好和注册Github时用的用户名和邮箱保持一致）
```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
## 远程仓库
### 分类
- 国外：[Github](https://github.com/)【推荐】
- 国内：[Gitee](https://gitee.com/)
### 问题
Github的服务器在国外，所以访问很慢。通过一个软件 [dev-sidecar](https://gitee.com/docmirror/dev-sidecar)（开发者边车）可以加速 Github提交 访问、Git 代码提交。
## 自建库并提交到Github远程仓库
```bash
git init # 初始化仓库
git add . # 将所有文件添加到仓库
git commit -m "first commit" # 将所有文件提交到仓库
git branch -M main # 创建主分支（main）
git remote add origin https://github.com/hs-young/pvp-hero-img.git # 连接远程仓库
git push -u origin main # 将代码提交到远程仓库
```
## Python 代码打包为桌面应用程序
pyinstaller：
```
pip install pyinstaller
```
打包
```
pyinstaller -F app.py -i favicon.ico
```