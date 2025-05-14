以下是 **常用 Git 命令总结**，包括从本地上传文件到 GitHub 的全流程命令：

---

### **一、基础配置**
1. **设置全局用户名和邮箱**（首次使用 Git 必做）
   ```bash
   git config --global user.name "YourName"
   git config --global user.email "your.email@example.com"
   ```

---

### **二、上传本地项目到 GitHub 全流程**
1. **初始化本地仓库**
   ```bash
   git init
   ```

2. **将文件添加到暂存区**
   ```bash
   git add .           # 添加所有文件
   git add filename    # 添加指定文件
   ```

3. **提交更改到本地仓库**
   ```bash
   git commit -m "提交说明"
   ```

4. **关联远程仓库**（需提前在 GitHub 创建空仓库）
   ```bash
   git remote add origin https://github.com/YourName/YourRepo.git
   # 或使用 SSH 地址：
   git remote add origin git@github.com:YourName/YourRepo.git
   ```

5. **推送代码到远程仓库**
   ```bash
   git push -u origin main   # 首次推送，设置默认上游分支
   git push                  # 后续推送简化命令
   ```

---

### **三、常用命令补充**
1. **查看仓库状态**
   ```bash
   git status
   ```

2. **查看提交历史**
   ```bash
   git log
   ```

3. **拉取远程仓库更新**
   ```bash
   git pull origin main
   ```

4. **分支操作**
   ```bash
   git branch                  # 查看分支
   git branch new-branch       # 创建新分支
   git checkout branch-name    # 切换分支
   git merge branch-name       # 合并分支
   ```

5. **撤销操作**
   ```bash
   git reset HEAD~1           # 撤销最近一次提交（保留修改）
   git checkout -- filename   # 撤销文件的未提交修改
   ```

6. **解决冲突后标记为已解决**
   ```bash
   git add filename           # 冲突解决后重新添加文件
   git commit -m "解决冲突"
   ```

---

### **四、完整上传流程示例**
```bash
# 初始化仓库
git init

# 添加文件并提交
git add .
git commit -m "初次提交"

# 关联远程仓库（替换成你的仓库URL）
git remote add origin https://github.com/YourName/YourRepo.git

# 推送代码
git push -u origin main
```

---

### **五、注意事项**
1. **GitHub 认证**：
   - 使用 HTTPS 协议时，首次推送需输入 **GitHub 用户名** 和 **Personal Access Token (PAT)**（[生成 PAT 教程](https://docs.github.com/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)）。
   - 使用 SSH 协议需提前配置 SSH 密钥（[SSH 配置指南](https://docs.github.com/authentication/connecting-to-github-with-ssh)）。

2. **首次推送失败**：
   - 若远程仓库有初始文件（如 README），需先执行：
     ```bash
     git pull origin main --allow-unrelated-histories
     ```

---

### **总结**
- **核心流程**：`git init` → `git add` → `git commit` → `git remote add` → `git push`
- **高频命令**：`status`, `log`, `pull`, `branch`, `checkout`

建议收藏此清单，随用随查！ 🚀