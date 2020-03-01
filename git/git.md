## git 使用总结

### 常用流程
![工作流程](./img/常规流程.png)

### 常见示例
* 普通模式`--no-ff`合并 和 `fast forward`合并有哪里不同  
普通合并后`git log --graph`有记录，而`fast forward`合并看不出来曾经做过合并
* git cherry-pick 可以在什么场景下使用  
线上存在bug，在一个分支上将bug修复后合并进行提交。另一个新开发功能分支利用`git cherry-pick [commitid]`则可同步修改bug内容
* git stash 存储的是哪一部分的内容  
存储的是工作区/暂存区的内容，即`git commit`前的内容
* 如何参与别人的功能开发 
```
本地新建分支并关联
1. git checkout -b dev origin/dev
2. git branch --set-upstream-to dev origin/dev

自动关联拉取远程分支
1. git pull
2. git checkout -b dev origin/dev
```
* 如何删除远程仓库的分支  
`git push origin --delete dev`
