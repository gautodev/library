##  将已有项目加入GitLab
的简要步骤

### 一、添加当前计算机的 ssh key
用于免密码使用 git push 等

- 重新打开一个 Git Bash
- 确认当前路径是用户目录后，输入以下命令：
```sh
ssh-keygen -t rsa
cat .ssh/id_rsa.pub
```
- 复制输出
- 登录 GitLab 网页，左侧选择`Profile Settings`，`SSH Keys`，粘贴到右边的`Key`里，并添加

### 二、push 到在 GitLab 上的新版本库

- 左侧`Projects`，选`New Project`，按提示继续
- 复制新项目的链接，形如 `git@xxxx:user/project.git`
- 在本地项目路径打开 Git Bash，输入命令
```sh
git remote add origin git@xxxx:user/project.git  # 替换为实际链接
git push origin master
```
