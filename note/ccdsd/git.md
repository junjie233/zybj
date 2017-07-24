## get里面的几个linux 命令

```sh
ls # 查看文件夹下的所有文件（不包涵隐藏文件）
ls -a # 查看文件夹下的所有文件，包含隐藏文件
ls -l # 查看文件夹下的所有文件 及文件夹的详细信息（文件大小的单位为B）
ls -alh # 查看文件的详细信息

## change directory

cd 目录名 # 进入指定的目标
    > 小技巧：
    > 命令行的自动补全（输入前面的几个字母，按‘tab’键进行补全）
cd .. # 返回上一级 和Css返回上一级相同
cd 路径 # 进入多级文件夹，如：cd/f/20170628/code/
cd 



## mkdir(make directory)创建文件夹
mkdir  加文件名  # 创建文件夹
mkdir  文件夹1 文件夹2 文件夹3  # 中间加空格创建多个文件夹
mkdir -p    aa/bb/cc  # 创建多级目录
mkdir --help  # 显示mkdir的所有使用方式



## 创建文件 （touch）
touch flie_name # 创建文件
touch css/idex.css # 创建多级文件（文件夹css必须存在）
touch index.js  app.js index.html 创建多个文件

vim file_name # 创建文件
vim css/index.css #创建多级文件（文件夹css必须存在）



## 修改文件名 （rename）
mv index.html a.html # 将index.html剪切粘贴在同一位置重命名为a.html，对文件夹同样适用

# 删除

## 删除文件(remove)
rm file_name # 删除文件 如：rm index.html
rm css/index.css # 删除多级文件

## 删除文件夹（remove directory）
rmdir css # 删除文件夹
rm -rf css/ (css/* 删除css下面的所有文件不包括css) # 递归删除，删除css文件夹和文件夹里面所有的文件


## 返回当前所在的路径 （print working directory）
pwd # 返回当前所在路径

清屏 `ctrl + l`
或者直接输入 clear
```


## vim编辑器
```sh
vim index.html
```
+ 首先进入的是交互模式
+ 按`i`进入`编辑模式`
+ 内容编辑完成后按`esc`退出编辑模式，进入交互模式
+ 输入`:wq`然后回车内容保存，然后找到目录检查内容
+ 不保存 `:q`

**在 `交互模式`模式下**
+ `dd`：删除整行
+ `yy`：复制整行到剪切板
+ `p`：将剪切板的东西粘贴到指定位置

+ 编辑模式
+ 命令模式
+ 交互模式



## git

### 版本管理系统
+ 分布式（git）
+ 集中式（svn）

分布式版本控制系统
### 创建版本库
```sh
git init

# 克隆远程仓库
git clone git@github.com:junjie233/gitck.git
```
### 将文件添加到缓存区
```sh
git add index.html
```

### 将缓存区的文件添加到版本库
```sh
git commit -m "新建index.html"
```

master分支（主分支，默认）
```sh
# 查看提交的记录
git log


get add. # 表示将所有的文件和文件夹添加到缓存区（空文件夹除外）
# 回到上一个版本
git reset --hard HEAD^（shift+6 ^） # 回到上一个版本
git seset --hard commit_id # 回到指定id版本

```
**查看哇恩健操作的状态**
```sh
git status # 查看文件的状态（红色表示未添加 ，绿色表示未提交）
```


### 配置远程仓库

```sh
# 添加远程仓库
git remote add  origin git@github.com:junjie233/gitck.git

# 查看远程仓库 
git remote show # 查看添加的所有远程仓库
git remote show origin # 查看origin这个远程仓库的详细信息
```
### 将本仓库文件推送到远程仓库
```sh
# 将远程仓库的文件pull到本地
git push  origin 