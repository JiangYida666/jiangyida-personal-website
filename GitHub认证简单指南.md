# GitHub认证简单指南 - 小白专用

## 问题说明

GitHub在2021年后不再允许使用账户密码进行Git操作，需要使用**Personal Access Token（个人访问令牌）**。

## 最简单的解决方案

### 方法一：使用GitHub Desktop（推荐给小白）

这是最简单的方法，不需要命令行！

1. **下载GitHub Desktop**
   - 访问：https://desktop.github.com/
   - 下载并安装GitHub Desktop

2. **登录GitHub账户**
   - 打开GitHub Desktop
   - 点击"Sign in to GitHub.com"
   - 使用浏览器登录您的GitHub账户

3. **上传代码**
   - 在GitHub Desktop中：File → Add Local Repository
   - 选择您的项目文件夹：`e:\高老师作业\个人网站`
   - 点击"Publish repository"
   - 输入仓库名称（如：`yida-personal-website`）
   - 点击"Publish Repository"

✅ **完成！** 代码会自动上传到GitHub，无需处理复杂的认证问题。

---

### 方法二：使用Git命令行（如果需要）

如果您想使用命令行，下面是简单步骤：

#### 第一步：生成Personal Access Token

1. 登录GitHub网站：https://github.com
2. 点击右上角头像 → **Settings**
3. 左侧菜单选择 **Developer settings**
4. 选择 **Personal access tokens** → **Tokens (classic)**
5. 点击 **Generate new token** → **Generate new token (classic)**

**填写信息：**
- Note: `我的个人网站项目`
- Expiration: `90 days`（推荐）
- Select scopes: 勾选 `repo`（全选）

6. 点击 **Generate token**
7. **立即复制生成的令牌**（只显示一次！）

#### 第二步：使用令牌上传代码

打开命令提示符（按Win+R，输入`cmd`），执行以下命令：

```cmd
cd "e:\高老师作业\个人网站"

git init
git add .
git commit -m "初始提交：个人网站"

git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main

# 这里会要求输入用户名和密码
# 用户名：您的GitHub用户名
# 密码：刚才复制的令牌（不是登录密码！）

git push -u origin main
```

## 常见问题解决

### 如果认证失败怎么办？

1. **检查令牌是否过期**：重新生成一个新令牌
2. **检查用户名是否正确**：确保输入的是GitHub用户名，不是邮箱
3. **检查仓库URL**：确保`你的用户名`和`仓库名`都正确

### 忘记令牌怎么办？

重新生成一个新令牌，旧的会自动失效。

## 推荐使用GitHub Desktop

对于Git新手，**强烈推荐使用GitHub Desktop**，因为：
- 图形化界面，简单直观
- 自动处理认证问题
- 不需要记忆复杂命令
- 错误提示更友好

## 后续操作

上传成功后，按照[作业提交指南.md](作业提交指南.md)中的步骤启用GitHub Pages即可。

---

**总结：使用GitHub Desktop是最简单的方法，完全避免命令行认证问题！** 🎯