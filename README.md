# GitHub Pages 部署指南

## 第一步：注册GitHub账号

1. 访问 [github.com](https://github.com)
2. 点击 "Sign up" 创建账号
3. 填写用户名、邮箱和密码
4. 完成邮箱验证

## 第二步：创建GitHub Pages仓库

1. 登录GitHub后，点击右上角的 "+" 号，选择 "New repository"
2. 仓库名称必须为：`你的用户名.github.io`
   - 例如：如果你的用户名是 `zhangsan`，仓库名就是 `zhangsan.github.io`
3. 选择 "Public"（公开）
4. 勾选 "Add a README file"
5. 点击 "Create repository"

## 第三步：上传文件到GitHub

### 方法一：通过GitHub网页界面上传

1. 进入你创建的仓库
2. 点击 "Add file" -> "Upload files"
3. 将以下文件和文件夹拖拽到上传区域：
   - `index.html`
   - `css/` 文件夹（包含 `style.css`）
   - `js/` 文件夹（包含 `main.js`）
   - `assets/` 文件夹（如果有图片等资源）
4. 在 "Commit changes" 中填写提交信息，例如："Initial commit"
5. 点击 "Commit changes"

### 方法二：使用Git命令行上传（推荐）

1. 安装Git：
   - Windows：从 [git-scm.com](https://git-scm.com/download/win) 下载安装
   - Mac：`brew install git`
   - Linux：`sudo apt-get install git`

2. 配置Git：
```bash
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

3. 在项目目录下初始化Git仓库：
```bash
cd github-portfolio
git init
```

4. 添加所有文件：
```bash
git add .
```

5. 提交更改：
```bash
git commit -m "Initial commit"
```

6. 添加远程仓库（替换为你的仓库地址）：
```bash
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
```

7. 推送到GitHub：
```bash
git branch -M main
git push -u origin main
```

## 第四步：访问你的网站

1. 等待1-2分钟让GitHub部署完成
2. 访问：`https://你的用户名.github.io`
3. 你的网站应该已经上线了！

## 第五步：自定义内容

### 修改个人信息
编辑 `index.html` 文件，替换以下内容：
- `[你的名字]` - 替换为你的真实姓名
- `your.email@example.com` - 替换为你的邮箱
- `+86 123 4567 8900` - 替换为你的电话
- `中国，北京` - 替换为你的地址

### 修改简历内容
在 `index.html` 的 `resume` 部分，修改：
- 工作经历
- 教育背景
- 证书与荣誉

### 添加你的作品
在 `portfolio` 部分：
- 修改项目标题和描述
- 添加项目标签
- 更新项目链接

### 添加博客文章
在 `blog` 部分：
- 修改文章标题、日期和描述
- 添加更多文章卡片

### 更新社交媒体链接
在 `contact` 部分：
- 更新GitHub、LinkedIn、Twitter链接

## 第六步：更新网站

每次修改文件后，使用以下命令更新：

```bash
git add .
git commit -m "Update website"
git push
```

GitHub会自动重新部署你的网站，通常1-2分钟后生效。

## 高级功能

### 自定义域名
1. 购买域名（如 example.com）
2. 在仓库中创建 `CNAME` 文件，内容为你的域名
3. 在域名服务商处配置DNS：
   - 添加A记录：`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - 或添加CNAME记录：`你的用户名.github.io`

### 启用HTTPS
1. 进入仓库设置
2. 找到 "Pages" 部分
3. 在 "Enforce HTTPS" 选项中选择启用

### 添加分析工具
在 `index.html` 的 `<head>` 部分添加：
- Google Analytics
- 百度统计
- 其他网站分析工具

## 常见问题

**Q: 网站无法访问？**
A: 检查仓库名称是否正确，必须为 `用户名.github.io`

**Q: 样式显示不正常？**
A: 确保 `css/` 和 `js/` 文件夹路径正确

**Q: 如何撤销更改？**
A: 使用 `git log` 查看历史，`git reset` 回退版本

**Q: 可以使用框架吗？**
A: 可以！GitHub Pages支持Jekyll、Hugo等静态网站生成器

## 项目结构

```
github-portfolio/
├── index.html          # 主页文件
├── css/
│   └── style.css      # 样式文件
├── js/
│   └── main.js        # JavaScript文件
└── assets/            # 图片等资源文件夹
```

## 下一步

- 添加更多个人照片到 `assets/` 文件夹
- 创建更多博客文章
- 添加项目截图
- 定期更新内容

祝你拥有一个精美的GitHub主页！