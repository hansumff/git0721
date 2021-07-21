# 步骤
 1. 全局配置

    ```
    git config --global user.name ""
    git config --global user.email ""

    ```

 2. 配置公钥
	```
	ssh-keygen -t rsa -C 
	提示生成在哪个文件夹 /home/xander/.ssh/id_rsa.pub
	进入github进行设置ssh

	```

3. 初始化仓库 git init
4. 从工作区放入暂存区 git add .
    ```
    warning: CRLF
    解决linux和window换行符不同：
    git config --global core.autocrlf false

    怎么查看是否放入暂存区
    git status
        绿色代表在暂存区
        红色代表在工作区(有修改)
    ```
5. 从暂存区到版本区 git commit -m ""

    ```
    版本回退：
    git reset --hard HEAD^ 回退一次
    git reset --hard 版本号
    git rm --cached x.txt 从暂存区删除文件
    ```

6. 分支

    ```
    git checkout -b dev 创建分支
    git branch 查看当前分支
    git checkout master 切换分支
    git merge dev 合并dev分支
    git branch -d dev 删除dev分支
    ```

7. github

    ```
    托管平台
    使用步骤:
        1. 创建仓库
        2. 建立远程链接 git remote add origin https://xxx.git
        3. 将本地文件提交到版本库
        4. 推送到远程仓库 git push -u origin master
    空项目克隆:
        1. git clone https://xxx.git
        2. 假如github新增了一个分支
        3. 本地执行git pull 会把所有分支拉回本地
        4. 此时有个问题，执行git branch查看不到新增分支
        5. 但是可以切换到该分支 git checkout xxx
    本地推送:
        1. 新修改后，把文件放到版本库，此时注意你在哪个分支下
        2. 执行git push origin xxx 
    ```
