# 工作坊推送链接平台 · 开发记录

> 工作坊现场即时推送资源的教师/学生双端平台
> 仓库：`vwen123/workshop`（main 分支）

---

## 📦 架构

| 档案 | 用途 |
|---|---|
| `teacher-panel.html` | 教师端（建立工作坊、推送链接/卡片）|
| `student-view.html` | 学生端（实时查看推送内容）|

- **后端**：Firebase Firestore（实时同步）
- **前端**：单文件 HTML（vanilla JS）
- **Firebase 项目**：workshop-cad98

---

## 🔑 关键功能

- 教师建立工作坊 + 推送链接 / 卡片给学生
- 学生端实时接收（Firebase 实时监听）
- 推送资源按时间戳排序
- 工作坊 / 卡片云端持久化

---

## 📝 迭代日志

### 已完成
- [x] Firebase 迁移到 workshop-cad98 项目
- [x] 云端保存 toast 提示
- [x] 工作坊 / 卡片永久持久化到 Firestore
- [x] 学生资源按推送时间戳排序
- [x] 修复 teacher-panel.html 空白 bug（2026-05-28）：`database.rules.json` 补加 `workshop` 路径权限；代码加 `.catch()` fallback 防止 Firebase 失败时页面全空

### brunei-foundation-workshop.html（2026-05-27 大幅迭代）
- [x] 共 30 张简报，GitHub Pages 部署：https://vwen123.github.io/workshop/brunei-foundation-workshop.html
- [x] Firebase 实时互动：check-in 便利贴（Slide 4）/ 文字云（Slide 28）/ checkout 便利贴（Slide 29），路径 `brunei-foundation/`
- [x] 全局字体缩小（clamp 系统）+ compact 类控制内容密集页
- [x] 背景纹理统一用 brunei-advanced 的 base64 JPEG
- [x] Slide 2：讲师简介（6项认证，照片 base64，t-name 20px normal）
- [x] Slide 3：三模块路线图（Canva AI / Gemini Storybook / NotebookLM）
- [x] Slides 4/28/29：T10 全高布局，输入框与内容区有 mt20 间距
- [x] 所有 Padlet 按钮去掉编号，统一为「📌 Upload to Padlet」
- [x] 所有 prompt-box 加入「📋 Copy Prompt」按钮（右下角，navigator.clipboard，2秒反馈）
- [x] Slide 23（新）：What Is Data Extraction? — 📂→💬→✨ 概念流
- [x] Slide 24（新）：Generate Infographic/Slide Deck — 3步Demo，无Padlet/Copy按钮
- [x] Slide 25：Activity #5，prompt 改为 `with【   】style`，加 AI Style Prompt Generator 链接
- [x] Slide 26：Advanced Features 翻牌改为 Custom Personas / Power Add-Ons / AI Animation Video
- [x] Slide 27：成就卡改为 Canva AI / Bulk Certificates / Storybook / NLM Infographic & Slide Deck
- [x] 删除旧 slides 11, 13, 14, 18, 23（旧）, 25（旧）, 26（旧）
- [x] 简报大纲（中英）：`20260527_汶莱AI基础班_简报大纲.md` + `_EN.md`，存 drafts + Obsidian

---

## 🚀 部署流程

```bash
cd "/Users/weiwen/Library/CloudStorage/GoogleDrive-vivianeiwen123@gmail.com/我的云端硬盘/workshops/workshop"
git add -A
git commit -m "描述改动"
git push origin main
```
