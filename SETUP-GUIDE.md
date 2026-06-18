# LinguaPK - GitHub 部署指南

## 第一步：配置 Git 身份（只需一次）

打开终端，运行以下命令（替换为你的信息）：

```bash
cd "C:/Users/hejiani/WorkBuddy/20260617174859/lingua-pk"
git config user.name "你的GitHub用户名"
git config user.email "你的GitHub邮箱"
git add -A
git commit -m "Initial commit: LinguaPK"
```

## 第二步：在 GitHub 上创建仓库

1. 打开 https://github.com/new
2. Repository name: `lingua-pk`
3. Description: `Language learning PK app for Jiani & Léo`
4. 选择 **Public**（Léo 需要访问）
5. **不要**勾选 "Add a README"（已经有了）
6. 点击 **Create repository**

## 第三步：关联远程仓库并推送

```bash
git remote add origin https://github.com/你的用户名/lingua-pk.git
git push -u origin main
```

系统会弹出 GitHub 登录窗口，登录即可。

## 第四步：开启 GitHub Pages

1. 打开仓库页面 → **Settings** → **Pages**
2. Source 选择 **GitHub Actions**
3. 保存

已经配置好了自动部署 workflow（`.github/workflows/deploy.yml`），
每次 push 到 main 分支都会自动更新网站。

## 第五步：访问你的网站

部署完成后（约1-2分钟），访问：

```
https://你的用户名.github.io/lingua-pk/
```

## 邀请 Léo 协作

1. 仓库页面 → **Settings** → **Collaborators**
2. 点击 **Add people**
3. 输入 Léo 的 GitHub 用户名
4. Léo 会收到邮件邀请

Léo 克隆仓库后就可以直接编辑 `index.html` 并 push 修改了。

## 日常更新流程

```bash
# 编辑 index.html 后
cd "C:/Users/hejiani/WorkBuddy/20260617174859/lingua-pk"
git add -A
git commit -m "描述你做了什么改动"
git push
```

push 后 GitHub Pages 会自动更新。

## 记忆功能说明

- 所有学习进度保存在浏览器的 localStorage 中
- 每个设备/浏览器独立保存（你的手机和电脑进度分开）
- 清除浏览器数据会重置进度
- 换设备访问时进度不会同步（这是预期行为，保持简单）
