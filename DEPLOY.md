# 🚀 GitHub 部署快速指南

## 方法一：通过 GitHub 网页界面（推荐新手）

### 步骤 1：创建 GitHub 账号
如果还没有 GitHub 账号，请先到 https://github.com 注册一个免费账号。

### 步骤 2：创建新仓库
1. 登录 GitHub
2. 点击右上角的 `+` 号
3. 选择 `New repository`
4. 填写信息：
   - Repository name: `winter-solstice-tangyuan` （或你喜欢的名字）
   - Description: `冬至汤圆团圆活动网页`
   - 选择 `Public` (公开)
   - ✅ 勾选 `Add a README file`
5. 点击 `Create repository`

### 步骤 3：上传文件
1. 在仓库页面，点击 `Add file` → `Upload files`
2. 将以下文件拖入或选择上传：
   - `index.html`
   - `README.md`
   - `LICENSE`
   - `.gitignore`
3. 在底部填写提交信息：`初始提交`
4. 点击 `Commit changes`

### 步骤 4：启用 GitHub Pages
1. 在仓库页面，点击 `Settings`（设置）
2. 在左侧菜单找到 `Pages`
3. 在 `Source` (来源) 部分：
   - Branch: 选择 `main`
   - Folder: 选择 `/ (root)`
4. 点击 `Save` (保存)
5. 等待 1-3 分钟

### 步骤 5：访问你的网页 🎉
你的网页地址为：
```
https://你的用户名.github.io/winter-solstice-tangyuan/
```

例如，如果你的用户名是 `xiaoming`，网址就是：
```
https://xiaoming.github.io/winter-solstice-tangyuan/
```

---

## 方法二：使用 Git 命令行（适合熟悉 Git 的用户）

### 前提条件
- 已安装 Git
- 已有 GitHub 账号

### 操作步骤

```bash
# 1. 在 GitHub 网页上创建一个新的空仓库（不要添加 README）

# 2. 在本地创建项目文件夹
mkdir winter-solstice-tangyuan
cd winter-solstice-tangyuan

# 3. 将下载的所有文件放入此文件夹
# (index.html, README.md, LICENSE, .gitignore)

# 4. 初始化 Git 仓库
git init

# 5. 添加所有文件
git add .

# 6. 创建第一个提交
git commit -m "初始提交：冬至汤圆活动网页"

# 7. 连接到 GitHub 远程仓库
git remote add origin https://github.com/你的用户名/winter-solstice-tangyuan.git

# 8. 推送到 GitHub
git branch -M main
git push -u origin main

# 9. 在 GitHub 网页上启用 Pages（参考方法一的步骤4）
```

---

## 📌 重要提示

1. **文件必须命名为 `index.html`**
   - GitHub Pages 会自动将 `index.html` 识别为首页

2. **仓库必须是 Public（公开）**
   - 免费用户只能为公开仓库启用 GitHub Pages
   - 私有仓库需要 GitHub Pro 订阅

3. **等待发布时间**
   - 首次发布需要等待 1-5 分钟
   - 后续更新一般 30 秒内生效

4. **检查部署状态**
   - 在仓库的 `Actions` 标签页可以看到部署进度
   - 绿色 ✓ 表示部署成功

---

## 🔄 如何更新网页内容

### 方法 A：通过 GitHub 网页
1. 在仓库中找到 `index.html`
2. 点击文件，然后点击右上角的铅笔图标 ✏️
3. 修改内容
4. 点击 `Commit changes`
5. 等待 30 秒，刷新网页查看更新

### 方法 B：通过 Git 命令
```bash
# 1. 修改本地文件

# 2. 提交更改
git add .
git commit -m "更新网页内容"

# 3. 推送到 GitHub
git push
```

---

## ❓ 常见问题

### Q1: 为什么访问网址显示 404？
- 检查是否已启用 GitHub Pages
- 确认文件名是 `index.html`（不是 `index.htm` 或其他）
- 等待 3-5 分钟后重试

### Q2: 更新了内容但网页没变化？
- 清除浏览器缓存（Ctrl+F5 或 Cmd+Shift+R）
- 等待 1-2 分钟让 GitHub Pages 重新构建
- 检查 GitHub Actions 是否成功部署

### Q3: 可以使用自定义域名吗？
- 可以！在 Settings → Pages → Custom domain 中设置
- 需要在域名服务商处添加 DNS 记录

---

## 📞 需要帮助？

如果遇到问题，可以：
1. 查看 [GitHub Pages 官方文档](https://docs.github.com/pages)
2. 在本仓库提交 Issue
3. 搜索相关问题的解决方案

---

🎉 **祝你部署成功！冬至快乐！** 🍡
