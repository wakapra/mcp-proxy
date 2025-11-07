# mcp-proxy

## 如何删除仓库里的文件 (How to Delete Files in the Repository)

本文档介绍了如何从 Git 仓库中删除文件的几种方法。

### 方法一：使用 Git 命令行删除文件

#### 1. 删除文件并从仓库中移除

如果你想删除一个文件并将此更改提交到仓库：

```bash
# 删除文件
git rm 文件名

# 提交更改
git commit -m "删除文件"

# 推送到远程仓库
git push
```

#### 2. 仅从 Git 跟踪中移除文件，保留本地文件

如果你想将文件从 Git 跟踪中移除，但保留本地文件：

```bash
# 从 Git 跟踪中移除，但保留本地文件
git rm --cached 文件名

# 提交更改
git commit -m "停止跟踪文件"

# 推送到远程仓库
git push
```

#### 3. 删除整个目录

删除一个目录及其所有内容：

```bash
# 删除目录
git rm -r 目录名

# 提交更改
git commit -m "删除目录"

# 推送到远程仓库
git push
```

### 方法二：通过 GitHub 网页界面删除

1. 在 GitHub 上打开你的仓库
2. 导航到要删除的文件
3. 点击文件右上角的 "..." 菜单
4. 选择 "Delete file"
5. 在提交消息框中输入删除原因
6. 点击 "Commit changes" 按钮

### 注意事项

- 删除文件前请确保该文件不再需要，因为删除操作是永久性的（除非从 Git 历史记录中恢复）
- 如果文件包含敏感信息，删除后它仍会保留在 Git 历史记录中。如需完全删除，请参考 Git 的历史记录清理工具
- 删除操作会影响所有协作者，请在删除重要文件前与团队沟通

---

## How to Delete Files in the Repository (English)

This document explains several methods to delete files from a Git repository.

### Method 1: Delete Files Using Git Command Line

#### 1. Delete a file and remove it from the repository

To delete a file and commit this change to the repository:

```bash
# Delete the file
git rm filename

# Commit the change
git commit -m "Delete file"

# Push to remote repository
git push
```

#### 2. Remove a file from Git tracking but keep the local file

To remove a file from Git tracking while keeping the local copy:

```bash
# Remove from Git tracking but keep local file
git rm --cached filename

# Commit the change
git commit -m "Stop tracking file"

# Push to remote repository
git push
```

#### 3. Delete an entire directory

To delete a directory and all its contents:

```bash
# Delete directory
git rm -r directory_name

# Commit the change
git commit -m "Delete directory"

# Push to remote repository
git push
```

### Method 2: Delete via GitHub Web Interface

1. Open your repository on GitHub
2. Navigate to the file you want to delete
3. Click the "..." menu in the upper right corner of the file
4. Select "Delete file"
5. Enter a commit message explaining the deletion
6. Click the "Commit changes" button

### Important Notes

- Ensure the file is no longer needed before deletion, as the operation is permanent (unless recovered from Git history)
- If a file contains sensitive information, it will remain in Git history even after deletion. For complete removal, refer to Git history cleaning tools
- Deletion affects all collaborators, so communicate with your team before removing important files