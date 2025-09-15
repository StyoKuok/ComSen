# 压缩感知学术进展网站

一个现代化、高级的压缩感知学术网站，基于Jekyll构建，专为GitHub Pages优化。

## ✨ 特性

- 🎨 **极其高级的现代化设计**：渐变背景、毛玻璃效果、动画过渡
- 📱 **完全响应式布局**：适配所有设备和屏幕尺寸
- 🧮 **数学公式支持**：使用MathJax渲染LaTeX数学公式
- ⚡ **高性能优化**：懒加载、预加载、代码分割
- 🌟 **粒子背景效果**：动态交互式背景动画
- 🔍 **SEO优化**：结构化数据、meta标签、sitemap
- 🎯 **可访问性友好**：WCAG 2.1兼容
- 🚀 **GitHub Pages就绪**：一键部署到GitHub Pages

## 🚀 快速开始

### 本地开发

1. **安装依赖** (需要Ruby环境)
```bash
# 安装Jekyll和Bundler
gem install jekyll bundler

# 安装项目依赖
bundle install
```

2. **启动开发服务器**
```bash
bundle exec jekyll serve
```

3. **访问网站**
```
http://localhost:4000
```

### GitHub Pages部署

1. Fork或下载此仓库
2. 在GitHub仓库设置中启用GitHub Pages
3. 选择源分支为 `main` 或 `master`
4. 网站将自动构建并发布

## 📁 项目结构

```
CompressedSensing/
├── _config.yml          # Jekyll配置文件
├── _layouts/            # 页面布局模板
│   ├── default.html     # 默认布局
│   ├── page.html        # 页面布局
│   └── post.html        # 文章布局
├── _pages/              # 静态页面
│   ├── what-is-cs.md    # 什么是压缩感知
│   ├── core-theory.md   # 核心理论
│   ├── algorithms.md    # 算法详解
│   ├── applications.md  # 实际应用
│   ├── learning-resources.md # 学习资源
│   └── about.md         # 关于我们
├── _posts/              # 博客文章
│   └── 2025-06-21-latest-developments.md
├── assets/              # 静态资源
│   ├── css/
│   │   └── style.css    # 主样式文件
│   ├── js/
│   │   └── main.js      # 主JavaScript文件
│   └── images/
│       └── favicon.svg  # 网站图标
├── index.md             # 首页
├── 404.html             # 404错误页面
└── Gemfile              # Ruby依赖
```

## 🎨 设计特色

### 视觉设计
- **现代化配色方案**：深色主题配合渐变色彩
- **玻璃拟态效果**：毛玻璃背景和透明度层次
- **动态粒子背景**：交互式粒子动画系统
- **流畅动画**：CSS3和JavaScript驱动的平滑过渡

### 交互体验
- **智能导航**：自动隐藏/显示的导航栏
- **平滑滚动**：页面内锚点平滑跳转
- **悬停效果**：丰富的鼠标交互反馈
- **自定义光标**：跟随鼠标的光晕效果

### 技术特性
- **MathJax集成**：完美渲染数学公式
- **代码高亮**：支持多种编程语言
- **SEO优化**：结构化数据和meta标签
- **性能优化**：资源压缩和缓存策略

## 🛠️ 自定义配置

### 修改网站信息
编辑 `_config.yml` 文件：
```yaml
title: 你的网站标题
description: 网站描述
email: your-email@example.com
github_username: your-github-username
```

### 添加新页面
1. 在 `_pages/` 目录下创建新的Markdown文件
2. 添加YAML前置内容：
```yaml
---
layout: page
title: 页面标题
description: 页面描述
permalink: /your-page/
---
```

### 发布新文章
1. 在 `_posts/` 目录下创建文件，格式：`YYYY-MM-DD-title.md`
2. 添加YAML前置内容：
```yaml
---
layout: post
title: 文章标题
author: 作者名
date: YYYY-MM-DD HH:MM:SS +TIMEZONE
categories: [category1, category2]
tags: [tag1, tag2]
description: 文章描述
---
```

## 🎯 SEO优化

网站已内置多项SEO优化：
- 结构化数据标记
- Open Graph标签
- Twitter Cards
- 自动生成sitemap.xml
- RSS feed支持
- 语义化HTML结构

## 📱 响应式设计

支持所有主流设备：
- 桌面端 (1200px+)
- 平板端 (768px-1199px)
- 手机端 (< 768px)

## 🌟 浏览器支持

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📄 许可证

MIT License - 详见 [LICENSE](LICENSE) 文件

## 🤝 贡献

欢迎提交问题和改进建议！

1. Fork 此仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送分支 (`git push origin feature/AmazingFeature`)
5. 创建Pull Request

## 📞 联系我们

- 网站：[您的网站URL]
- 邮箱：contact@compressedsensing.org
- GitHub：[@your-username](https://github.com/your-username)

---

⭐ 如果这个项目对您有帮助，请给我们一个Star！
