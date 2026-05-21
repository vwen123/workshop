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

---

## 🚀 部署流程

```bash
cd "/Users/weiwen/Library/CloudStorage/GoogleDrive-vivianeiwen123@gmail.com/我的云端硬盘/workshops/workshop"
git add -A
git commit -m "描述改动"
git push origin main
```
