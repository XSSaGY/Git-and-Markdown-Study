# 使用GitHub的步骤
- 添加文件
- 选择第一个commit directly to the master branch
- 然后等待一会儿，会在存储库中出现compare and pull request按钮，点击它
- 填写pull request的标题和描述，然后点击create pull request按钮
- 如果是自己的项目则可以直接点击merge pull request按钮，如果是其他人的项目则需要等待项目所有者合并代码
- 完成！

# 使用命令行上传Github仓库
- 首先安装git，并配置好ssh
- 在本地创建仓库，并将本地仓库与远程仓库关联
- 在本地仓库中添加文件，并提交到本地仓库
- 推送本地仓库到远程仓库
- 然后执行下面代码

```shell
git init
git add . # 添加当前目录所有文件，不包括文件删除
git add -A # 添加所有文件
git add -u # 添加所有变动文件
git commit -m "commit content" 
git commit # 打开默认编辑器输入commit内容
git remote add origin <EMAIL>:username/repository.git # 关联远程仓库SSH地址
git push -u origin master # 推送本地仓库到远程仓库，-u参数是关联远程仓库和本地仓库的master分支
git push # 推送当前分支
git checkout -b new_branch # 创建并切换到新分支
git branch -d new_branch # 删除分支

# 在新分支上提交和上面相同
# pull / add / commit / push 等命令的详细用法请参考git官方文档
```