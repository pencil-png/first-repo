# git的基本概念

### git初始化指令

git init，在文件中会生成.git文件（隐藏式文件）<br>

---

### git的基本操作

git分为工作区和暂存区和本地仓库，远程仓库

- 工作区：文件实际修改的地方
- 暂存区：通过git add指令将文件上传至暂存区，git add .表示上传全部修改的文件
- 本地仓库（repository）：通过git commit -m "消息内容"将暂存区的文件上传至本地仓库
- 远程仓库（remote repository）：git push，将本地仓库的文件上传至远程仓库

---

1. **一次commit只能有一条message，所以多个文件要一次一次进行commit**

---

1.  git remote add origin（仓库的别名，后面使用更加方便） <url>
2.  git pull origin main --allow-unrelated-histories 先拉取远程代码解决冲突（因为远程代码有本地没有的东西）
3.  git push -u origin main
4.  现在使用SSH密钥进行操作，git remote set-url git@github.com:pencil-png/first-repo.git
5.  怎么没反应
6.  原来是ssh拒绝连接22端口，导致无法同步到远程，现在将ssh修改为http
7.  学习使用vscode集成git，在源代码管理部分
8.  如何在项目中添加git
    - 把远程项目的git相关文件copy过来
    - 在项目里面通过git bash中初始化

## git的分支

## 关于git中不需要提交的文件，怎么处理

在.gitignore文件中写不需要的文件，格式如下：

1. \*.txt表示所有后缀为.txt的文件都不push(忽略)
2. ！build.txt表示，除了该文件，其他的都忽略
3. /temp表示根目录下的temp文件或文件夹忽略，但是其他文件里面的temp子目录不会忽略
4. temp/表示所有名为temp的文件夹忽略，**但是不会忽略名为temp的文件！！！**
5. 忽略某个文件，直接写文件名，例如：.env,passport.txt
6. 忽略文件夹里的所有内容，但保留文件夹:cache/\*
7. 忽略某个路径下的文件，src/temp/.js
