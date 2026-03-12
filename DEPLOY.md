# 知行中国文档网站部署指南

## 🚀 快速部署方案

### 方案A：GitHub Pages（推荐）
1. **创建GitHub仓库**
   ```bash
   # 仓库名建议：zhixing-china-docs
   # 描述：知行中国项目文档中心
   ```

2. **推送代码到GitHub**
   ```bash
   git init
   git add .
   git commit -m "初始提交：知行中国项目文档"
   git branch -M main
   git remote add origin https://github.com/[你的用户名]/zhixing-china-docs.git
   git push -u origin main
   ```

3. **启用GitHub Pages**
   - 进入仓库设置 → Pages
   - 分支选择：`main`
   - 文件夹选择：`/(root)`
   - 保存后等待部署完成

4. **访问地址**
   ```
   https://[你的用户名].github.io/zhixing-china-docs
   ```

### 方案B：Netlify（更专业）
1. **注册Netlify账户**（免费）
2. **拖拽web-docs文件夹到Netlify**
3. **自动部署完成**
4. **获得自定义域名**（如：zhixing-china.netlify.app）

### 方案C：Vercel（最快）
1. **注册Vercel账户**（免费）
2. **导入GitHub仓库**
3. **自动部署完成**
4. **获得自定义域名**（如：zhixing-china.vercel.app）

## 📁 网站结构

```
web-docs/
├── index.html              # 网站首页
├── _config.yml            # GitHub Pages配置
├── .nojekyll              # 禁用Jekyll处理
├── DEPLOY.md              # 部署指南（本文件）
├── 文档/                  # 所有项目文档
│   ├── *.md              # Markdown文档
│   ├── *.pptx            # PowerPoint文件
│   └── *.pdf             # PDF文件
├── 项目/                  # 项目相关文件
│   └── 知行中国/
│       └── README.md     # 项目README
└── README.md             # 工作空间说明
```

## 🔗 文档链接

所有文档都可以通过以下方式访问：

### 在线访问：
- **首页：** `https://[域名]/`
- **具体文档：** `https://[域名]/文档/[文件名]`
- **项目文件：** `https://[域名]/项目/[路径]`

### 本地访问：
- 打开 `index.html` 文件
- 或使用本地服务器：
  ```bash
  cd web-docs
  python3 -m http.server 8000
  # 然后访问 http://localhost:8000
  ```

## 🔄 更新流程

### 添加新文档：
1. 将新文档放入 `web-docs/文档/` 目录
2. 在 `index.html` 中添加对应的卡片
3. 提交并推送到GitHub
4. GitHub Pages会自动更新（约1-2分钟）

### 更新现有文档：
1. 直接修改 `web-docs/文档/` 中的文件
2. 提交并推送到GitHub
3. 网站自动更新

### 修改网站样式：
1. 编辑 `index.html` 中的CSS部分
2. 测试本地效果
3. 提交并推送

## 📊 网站功能

### 已实现功能：
- ✅ 响应式设计（手机、平板、电脑）
- ✅ 文档分类展示（核心文档、竞品分析、项目执行）
- ✅ 状态标签（已完成、进行中、待开始）
- ✅ 文档元数据显示（字数、时间）
- ✅ 自动更新时间显示
- ✅ 文档点击统计（控制台）

### 计划功能：
- 🔄 搜索功能（可通过Algolia集成）
- 🔄 文档版本历史
- 🔄 评论功能（可通过Disqus集成）
- 🔄 访问统计（可通过Google Analytics集成）

## 🔧 技术细节

### 使用技术：
- **HTML5** + **CSS3**（纯静态，无框架依赖）
- **JavaScript**（少量交互功能）
- **GitHub Pages**（免费托管）
- **Markdown**（文档格式）

### 浏览器兼容性：
- Chrome 60+ ✅
- Firefox 60+ ✅  
- Safari 12+ ✅
- Edge 79+ ✅
- iOS Safari 12+ ✅
- Android Chrome 60+ ✅

## 📝 维护说明

### 定期维护：
1. **每日更新**：添加新产出文档
2. **每周整理**：清理旧版本，更新分类
3. **每月回顾**：更新项目进展总览

### 备份策略：
1. **本地备份**：`web-docs` 文件夹完整备份
2. **Git备份**：推送到GitHub作为版本控制
3. **云备份**：可同步到Google Drive/OneDrive

## 🆘 故障排除

### 常见问题：

#### 1. 网站无法访问
- 检查GitHub Pages设置是否正确
- 确认仓库是公开的（或你有访问权限）
- 等待几分钟让部署完成

#### 2. 文档链接失效
- 检查文件路径是否正确
- 确认文件已推送到仓库
- 文件名不要包含特殊字符

#### 3. 样式显示异常
- 清除浏览器缓存
- 检查CSS文件是否加载
- 确认HTML结构正确

#### 4. 更新后不生效
- GitHub Pages部署需要1-2分钟
- 强制刷新页面（Ctrl+F5）
- 检查GitHub Actions状态

## 📞 支持与联系

### 网站维护：
- **负责人**：小青工作助手
- **更新频率**：实时更新（有新文档立即添加）
- **问题反馈**：通过项目负责人全真联系

### 技术问题：
- GitHub Issues：在仓库中创建Issue
- 邮件支持：通过项目邮箱联系
- 即时沟通：通过工作群组联系

---

*最后更新：2026-03-12 | 维护者：小青*