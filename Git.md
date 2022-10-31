# Git

## 文件

### 三种状态

- 已提交 committed

	- 已安全存入本地数据库

- 已修改 modified

	- 改动但尚未提交

- 已暂存 staged

	- 对已修改文件的当前版本做出标识激情期加入下一次提交的快照中

### 状态

- 已跟踪

	- 未修改
	- 已修改
	- 已暂存

- 未跟踪

## 工作流

### 工作流

- 1 修改工作目录的文件
- 2 暂存文件,将文件快照加入暂存区
- 3 提交暂存区的文件,将快照永久保存在Git目录(仓库)中

## 命令行

### 配置

- 三级

	- 1 /etc/config

		- 所有用胡及其仓库的值, 命令加入--system可以修改

	- 2 !/.gitconfig ~/.config/git/config

		- 用户自己的

	- 当前的config

		- 针对的是本仓库

### 配置方法

- git config --global user.name "xxx"
- git config --global user.email "xxx"
- git config --global user.name

	- 是查看信息而不是设置

- git config core.editor xxx

	- 默认的文本编辑器
	- 甚至可以加入路径和命令
	- git config --global core.editor "E:\Program Files\Microsoft VS Code\code.exe"

- git config --list

	- 查看所有的用户配置
	- 会从不同文件读取键值对,会使用最后面的键值对

### 方法

- 帮助

	- git help <>
	- git <> --help
	- man git-<>

		- windows 没有哦

### 仓库

- 初始化 

	- git init

		- 初始化一个仓库

- 添加

	- git add [*+]

		- 即跟踪新的文件
		- 暂存已修改的文件

- 提交

	- git commit

		- commit是已经暂存(add)的版本

- 克隆

	- git clone [url] [dictionary]

		- 对仓库的所有文件进行获取, 放到指定的仓库

- 文件状态

	- git status

		- 简洁状态 -s/--short

			- 左 是否已暂存
			- 右 是否已修改
			- 新添加的未跟踪文件前面有 ?? 标记
			- 新添加到暂存区中的文件前面有 A 标记，
			- 修改过的文件前面有 M标记。
			- M 有两个可以出现的位置，出现在右边的 M 表示该文件被修改了但是还没放入暂存区，出现在靠左边的 M 表示该文件被修改了并放入了暂存区。
			- 输出标记会有两列,第一列是对staging区域而言,第二列是对working目录而言。

## 分支主题 4

