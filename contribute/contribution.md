# 贡献流程<a name="ZH-CN_TOPIC_0000001052970939"></a>

## 环境准备<a name="section124971410183614"></a>

-   针对Git的安装、环境配置及使用方法，请参考GitCode帮助中心的Git知识大全：[https://docs.gitcode.com/docs/help/home/general-reference/git](https://docs.gitcode.com/docs/help/home/general-reference/git)
-   注册SSH公钥，请参考GitCode帮助中心的公钥管理：[https://docs.gitcode.com/docs/help/home/user_center/security_management/ssh](https://docs.gitcode.com/docs/help/home/user_center/security_management/ssh)
-   在开展GitCode的工作流之前，您需要先在Cangjie的代码托管平台上找到您感兴趣的Repository。

## 代码下载<a name="section6125202333611"></a>

### 从云上Fork代码分支<a name="section8365811818"></a>

1.  找到并打开对应Repository的首页。
2.  点击右上角的 Fork 按钮，按照指引，建立一个属于**个人**的云上Fork分支。

###  把Fork仓下载到本地<a name="section49051646201819"></a>

请按照以下的过程将Repository内的代码下载到您的在计算机上：

1.  **创建本地工作目录**：

    您需要创建本地工作目录，以便于本地代码的查找和管理

    ```
    mkdir ${your_working_dir}
    ```

2.  **复制远程仓库到本地**
    1.  **切换到本地路径**

        ```
        mkdir -p ${your_working_dir}
        cd ${your_working_dir}
        ```

    2.  **复制远程仓库到本地**
        -   您可以在仓库页面内复制远程仓库的拷贝地址，得到`$remote\_link`：

            **图 1**  复制远程仓库
            
            ![image.png](https://raw.gitcode.com/user-images/assets/3162607/83364454-06ef-4f0c-a991-45855679528c/image.png 'image.png')

        -   在本地电脑执行拷贝命令：

            ```
            git clone $remote_link
            ```

### 代码提交\(git clone场景\)<a name="section669715742719"></a>

1.  **拉分支**

    更新您的本地分支

    ```
    git remote add origin $remote_link
    git fetch origin
    git checkout master  
    git pull --rebase 
    ```

    基于远端master分支拉取本地调试分支

    ```
    git branch myfeature origin/master
    git checkout myfeature  
    ```

    然后在myfeature分支上编辑和修改代码。

2. **在本地工作目录提交变更**

   ```
   git add .
   git commit -sm  "xxxxxx"  // 提交信息包含signoff邮箱
   ```

   您可能会在前次提交的基础上，继续编辑构建并测试更多内容，可以使用commit --amend继续添加提交。

3.  **将变更推送到您的远端目录**

    准备进行审查（或只是建立工作的异地备份）时，将分支推到您的fork仓库:

    ```
    git push -f origin myfeature
    ```

## 创建Pull Request<a name="section28261522124316"></a>

访问您的fork仓页面，点击创建Pull Request按钮选择myfeature分支生成PR。

详细操作请参考GitCode帮助中心的开发协作指导：[https://docs.gitcode.com/docs/help/home/org_project/pullrequests/pr-create](https://docs.gitcode.com/docs/help/home/org_project/pullrequests/pr-create)


## 门禁构建<a name="section981124754415"></a>

### 创建Issue<a name="section979820334458"></a>

1.  找到并打开对应Repository的首页
2.  选择左上角的Issues页签，点击右侧新建Issue按钮，按照指引建立一个专属的任务，用于相关联的代码（开发特性/修改bug）执行CI门禁。

### 将Issue与PR关联<a name="section5470144853615"></a>

创建PR或编辑已有的PR时，描述框输入\#+I+五位Issue ID，即可将Issue与PR关联。

**约束：**

-   需要达到最低评审人数。
-   评审问题全部解决才能合入。
-   禁止合入自己创建的 Pull Request。
-   合并 PR 前需确保关联的流水线任务成功运行并通过检查。

### 触发代码门禁<a name="section11163175420406"></a>

门禁执行完成，会在该Issue关联的所有PR中自动评论门禁执行结果。


## CI门户<a name="section8563257123985"></a>

Cangjie通过持续集成（CI，Continuous Integration）及时发现代码问题，确保代码质量可靠和功能稳定，包括：

- 代码门禁：开发者向Cangjie提交代码合入申请后，会触发门禁检查，例如静态检查、代码编译、功能测试等，门禁通过后才能合入代码。
- 每日构建：Cangjie的持续集成流水线每日自动执行，以便提前发现代码静态检查、编译、功能等方面的问题，及时修复问题，确保代码质量。

