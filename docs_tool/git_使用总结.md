## Git使用总结

### 1. 代码push至多个git仓库

1. 新建仓库，假设新地址为：```ssh://git@git.github.com/~zhouyong03/mtdeal-ranker-bottom.git```
2. 进入本地项目目录，执行：```git remote add another ssh://git@git.github.com/~zhouyong03/mtdeal-ranker-bottom.git```
3. 上传即可：```git push another offline(branch)```

### 2. git submodule

命令：```git submodule add <git_url> <local_dir>```

含义：添加```repo_url``` 项目 更新至 ```local_dir```中.

> 项目目录下的```.gitmodules```和```.git/config```内容是由```git submodule add ...```命名执行后生成的，人工改动无效。

git submodule详解 参考： http://www.360doc.com/content/13/0110/10/7991404_259310693.shtml

### 2. git branch

以```dev```分支为例：

+ 删除远程分支：```git push origin :dev```
+ 删除本地分支：```git branch -d dev```