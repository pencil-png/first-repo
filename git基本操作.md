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

1. git remote add origin（仓库的别名，后面使用更加方便） <url>
2. git pull origin main --allow-unrelated-histories 先拉取远程代码解决冲突（因为远程代码有本地没有的东西）
3. git push -u origin main
