## Git使用总结

### 代码上传至多个git仓库

1. 新建仓库，假设地址为：```ssh://git@git.github.com/~zhouyong03/mtdeal-ranker-bottom.git```
2. 进入本地项目目录，执行：```git remote add another ssh://git@git.github.com/~zhouyong03/mtdeal-ranker-bottom.git```
3. 上传即可：```git push another offline(branch)```