# Study-Supervision-Plan
## 📚✨ 合作打卡学习计划

合作打卡，每日精进。监督学习，赛博飞升。🙏

本项目 为自记录打卡项目，追踪规律性学习计划。

## 📅 每日打卡计划
📒 **asset**  是一个资产库，您可以随意添加想要的资产，后续也可以是.accdb .r .xl .dpxi等文件的存放区域
--|📷 **image** 是一个图片库，您可以将想要上传的照片上传至此，插入请使用相对路径，例如24.10.17.1.jpg插入应为如下方式
  ```markdown
    ![Image](../asset/image/24.10.17.1.jpg)
  ```
📝 **日报** 日报是自记录的文件夹，平常我就有在markdown记日记的习惯，我会将一天的内容简要记录，并<span style="color: red;">标记</span>问题或待解决的方案，
语法如下：
```markdown
<span style="color: red;">这是红色text</span>
```
👆🤓 诶 是的！ 都2024年了，Github在线预览还是不能变红，建议本地打开  
<span style="color: green;">当然，您也可以根据自己习惯选择其他方式</span>

 🎯 **目标** 是一个长期计划文件，您可以自由添加和修改您的长期目标。后续也可以作为制定子目标、跟踪进度的存放区域，并支持记录各种格式的文件，如 .txt, .md, .pdf, .xlsx 等，用于详细描述目标和计划的各个阶段。  

✨ *"The trouble with not having a goal is that you can spend your life running up and down the field and never score."*


💡 学习内容  
⌨ 编程语言：Java, Python，Dart, Haskell  
🛠️ 开发工具：VsCode, Git 
🗄️  数据库管理：AWSDB, MongoDB  

🙌 合作者 
- [Mandy](https://github.com/Mandy-MM)
布里斯托大学 计算机科学本科大一在读  
主线：计算机体系结构，编程基础，离散数学  
爱好：寻找兴趣方向中🧐  
🚧 **施工中** 

- [Each](https://github.com/Each9084) 
布里斯托大学 数据科学硕士在读  
主线：学习**数据分析**相关的内容  
爱好：安卓开发，正在转向flutter，指不定什么时候发布一个bug，里面可能有些许app的痕迹  

---

## 🗳**Git的相关指令**

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
>  --hard参数表示重置工作区和暂存区， 
>  --soft参数表示重置暂存区，
>  --mixed参数表示重置工作区。

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



🚧 **其他共同学习细节正在施工中** 
