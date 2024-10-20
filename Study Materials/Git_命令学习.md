

# 🗳**Git的相关指令**

<img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" alt="Git Icon" width="100"/>

如果Mandy老师想系统地学习Git，安利B站GeekHour老师的课程：🔗[一小时Git教程](https://www.bilibili.com/video/BV1HM411377j/),省时省力，便于理解，快速入门

🎖️Markdown毕竟还是不太直观，建议Mandy老师和我当做查询的工具书，系统性学习还是跟着课程走  
✂️为了精简主页，未来随着学习越来越，待熟练掌握后，会将此教程转入专门的文件夹中😄

#### 初始化  (操作)

初始化设置用户名和邮箱

> 配置用户名

```markdown
git config --global user.name "Your Name"
```

> 配置邮箱

```markdown
git config --global user.email "mail@example.com" 
```

> 存储配置 可以在每次打开时都保存该配置

```markdown
git config --global credential store 
```



#### 创建仓库（操作）

> 省略project-name则在当前目录创建

```markdown
git init <project-name>
```

> 克隆一个远程仓库

```markdown
git clone <url>
```



#### 四个区域（概念）

- 四大区域是工作环境的基础概念

  > 工作区就是你在电脑里能实际看到的目录。

- 工作区（Working Directory）

  > 暂存区也叫索引， 用来临时存放未提交的内容， 一般在.git目录下的index中。

- 暂存区（Stage/Index）

  > Git在本地的版本库， 仓库信息存储在.git这个隐藏目录中。

- 本地仓库（Repository）

  > 托管在远程服务器上的仓库。 常用的有GitHub、 GitLab、 Gitee。

- 远程仓库（Remote Repository）



#### 文件状态（概念）

> 修改了但是没有保存到暂存区的文件。

```markdown
已修改（Modified）
```

> 修改后已经保存到暂存区的文件

```markdown
已暂存（Staged）
```

> 把暂存区的文件提交到本地仓库后的状态。

```markdown
已提交（Committed）
```



#### 仓库状态（概念）

> 默认主分支 👆🤓 诶 可能要问 逸老师：为什么既有main又有master呢？
> 答案是：有人吃的太饱了 觉得master含有歧视，所以后期Git组织改为了中立的main
> 所以看到自己是master不要疑惑，和main没有区别

```markdown
main/master 
```

> 默认远程仓库

```markdown
Origin
```

> 指向当前分支的指针

```markdown
HEAD
```

> 上一个版本

```markdown
HEAD^
```

> 上四个版本

```markdown
HEAD~
```

#### 特殊文件（概念）

> Git仓库的元数据和对象数据库

```markdown
.git
```

> 忽略文件，不需要提交到仓库的文件,例如一些存储密码或其他隐私的文档，

```markdown
.gitignore 
```

> 指向当前分支的指针

```markdown
.gitattributes 
```

> 使空目录被提交到仓库

```markdown
.gitkeep
```

> 记录子模块的信息

```markdown
.gitmodules 
```

> 记录仓库的配置信息

```markdown
.gitconfig 
```



#### *添加和提交(操作)

> 添加一个文件到暂存区， 比如git add . 就表示添加所有文件到暂存区

```markdown
git add <file>
```

> 提交所有暂存区的文件到本地仓库，message里一般会添加更新的信息

```markdown
git commit -m "message"
```

> 提交所有已修改的文件到本地仓库, 是前两者的合集，一般使用这个最方便

```markdown
git commit -am "message"
```

#### *合并和变基(操作)

> 合并用于将两个不同分支的修改合并在一起，通常是在完成新功能或修复后，将一个分支的更改合并到主分支中。合并会保留所有分支的历史记录。

```bash
git merge <branch>
```

> 变基用于将当前分支的更改重新应用到另一个分支的基础上，以保持提交历史的整洁、线性。它可以避免额外的合并提交，让历史记录看起来像是按顺序提交的。

```bash
git rebase <branch>
```

> git merge 和 git rebase 的区别：merge 会产生一个新的合并提交并保留分支历史，而 rebase 会将当前分支的提交重排到目标分支之后，不产生额外的合并提交。

<<<<<<< HEAD

#### *撤销和恢复（操作）

> 移动一个文件到新的位置。

```markdown
git mv <file> <new-file>
```

> 从工作区和暂存区删除一个文件， 并且将这次删除放入暂存区。

```markdown
git rm <file>
```

> 从索引/暂存区中删除文件， 但是本地工作区文件还在， 只是不希望这个文件被版本控 制。

```markdown
git rm --cached <file>
```

> 恢复一个文件到之前的版本。

```markdown
git checkout <file> <commit-id>
```

> 创建一个新的提交， 用来撤销指定的提交， 后者的所有变化将被前者抵消， 并且应用到 当前分支。

```markdown
git revert <commit-id>
```

> 重置当前分支的HEAD为之前的某个提交， 并且删除所有之后的提交。
> --hard参数表示重置工作区和暂存区， 
> --soft参数表示重置暂存区，
> --mixed参数表示重置工作区。

```markdown
git reset --mixed <commit-id>
```

> 撤销暂存区的文件， 重新放回工作区 （git add的反向操作）。

```markdown
git restore --staged <file>
```

#### *查看状态或差异

>查看仓库状态， 列出还未提交的新的或修改的文件。

```markdown
git status
```

>查看提交历史， --oneline表示简介模式。

```markdown
git log --oneline
```

>查看未暂存的文件更新了哪些部分。

```markdown
git diff 
```

>查看两个提交之间的差异。

```markdown
git diff <commit-id> <commit-id>
```

=======