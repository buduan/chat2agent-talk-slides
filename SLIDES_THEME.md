# Slidev 主题设计文档

## 设计理念

本主题采用**极简主义设计原则**，使用浅色背景配合天蓝色（Sky Blue）色系，营造专业、清晰的演示效果。

### 核心设计原则

1. **克制与精确**：避免过度装饰，每个元素都有明确目的
2. **一致的色彩体系**：统一使用 Sky Blue 色系，拒绝杂色
3. **精确的间距**：使用 8px 基础网格系统确保视觉协调
4. **清晰的层次**：通过字重、大小和透明度建立信息层次

## 色彩系统

### 主色调
- **主色**: `#0ea5e9` (Sky 500) - 用于链接、按钮、强调
- **深色**: `#0284c7` (Sky 600) - 用于 hover 状态、粗体文字
- **浅色**: `#e0f2fe` (Sky 100) - 用于卡片背景

### 辅助色
- **超浅色**: `#f0f9ff` (Sky 50) - 用于次要卡片
- **中等色**: `#bae6fd` (Sky 200) - 用于第三层级卡片
- **亮色**: `#38bdf8` (Sky 400) - 用于边框、图标

### 中性色
- **背景**: `#fafafa` - 页面主背景
- **表面**: `#ffffff` - 卡片、内容块背景
- **边框**: `#e2e8f0` - 分隔线、边框
- **正文**: `#0f172a` - 主要文字
- **次要**: `#475569` - 次要文字、说明
- **辅助**: `#94a3b8` - 提示、元信息

### 替代的色卡映射
- 原绿色 → Sky 100 (`#e0f2fe`)
- 原黄色 → Sky 50 (`#f0f9ff`)
- 原紫色 → Sky 200 (`#bae6fd`)
- 原红色 → Sky 400 (`#38bdf8`)
- 原粉色 → Sky 300 (`#7dd3fc`)

## 排版系统

### 字体栈
```
-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
"Helvetica Neue", Arial, "Noto Sans", sans-serif
```

### 标题层级
- **H1**: 2.5rem / 600 weight / -0.02em letter-spacing
- **H2**: 2rem / 600 weight / -0.01em letter-spacing
- **H3**: 1.5rem / 500 weight / normal letter-spacing

### 正文
- **基础**: 1rem / 1.6 line-height / 0.01em letter-spacing
- **小字**: 0.875rem / 1.5 line-height
- **大字**: 1.125rem / 1.6 line-height

### 标题定位
- **默认**: 左上角固定，不随内容移动
- **居中页面**: 标题居中显示
- **距顶**: 1.5rem
- **距左**: 2rem

## 间距系统

基于 8px 网格，使用 rem 单位：

- **0.25rem** (4px) - 极小间距
- **0.5rem** (8px) - 小间距、内联元素
- **0.75rem** (12px) - 紧凑间距
- **1rem** (16px) - 标准间距
- **1.5rem** (24px) - 舒适间距
- **2rem** (32px) - 大间距
- **3rem** (48px) - 超大间距

### 组件间距
- **卡片内边距**: 1.5rem
- **列表项间距**: 0.75rem
- **段落间距**: 1.5rem
- **代码块间距**: 1.5rem

## 卡片样式

### 标准卡片
```html
<div class="p-6 rounded-lg bg-sky-100 bg-opacity-50">
  内容
</div>
```

### 强调卡片
```html
<div class="p-6 rounded-lg bg-sky-200 bg-opacity-40">
  重要内容
</div>
```

### 次要卡片
```html
<div class="p-6 rounded-lg bg-sky-50 bg-opacity-60">
  补充信息
</div>
```

### 卡片特性
- 圆角: 0.5rem (8px)
- 边框: 1px solid rgba(14, 165, 233, 0.2)
- 阴影: 0 1px 3px rgba(0, 0, 0, 0.06)
- Hover: 阴影增强，轻微上移

## 布局系统

### 两栏布局
```markdown
---
layout: two-cols
---

# 左侧标题

左侧内容

::right::

右侧内容（无标题）
```

### 居中布局
```markdown
---
layout: center
class: text-center
---

# 居中标题

居中内容
```

## 组件样式

### 代码块
- 背景: `#f1f5f9`
- 边框: 1px solid `#e2e8f0`
- 圆角: 0.5rem
- 内边距: 1.25rem
- 字体: 等宽字体栈

### 表格
- 边框: 1px solid `#e2e8f0`
- 表头背景: `#e0f2fe`
- 表头文字: `#0284c7` + 600 weight
- 单元格内边距: 0.75rem 1rem

### 引用块
- 左边框: 3px solid `#0ea5e9`
- 内边距左侧: 1rem
- 颜色: `#475569`
- 样式: 斜体

### 按钮
- 背景: `#0ea5e9`
- 文字: 白色
- 内边距: 0.75rem 1.5rem
- 圆角: 0.5rem
- Hover 背景: `#0284c7`

## Mermaid 图表

推荐使用的 Sky Blue 色系：

```mermaid
style A fill:#f0f9ff
style B fill:#e0f2fe
style C fill:#bae6fd
style D fill:#7dd3fc
```

## 动效

### 全局过渡
- 时长: 0.2s
- 缓动: ease
- 属性: opacity, transform, box-shadow, border-color

### Hover 效果
- 卡片: 阴影增强 + Y轴 -2px
- 链接: 底部边框出现
- 按钮: 背景色加深

## 响应式

### 断点
- **桌面**: > 768px
- **移动**: ≤ 768px

### 移动适配
- 两栏布局变为单栏
- 标题字体缩小
- 内边距减小

## 使用指南

### 1. 避免的颜色
- ❌ 紫色 (purple)
- ❌ 绿色 (green) 
- ❌ 黄色 (yellow)
- ❌ 粉色 (pink)
- ❌ 红色 (red) - 非警示场景
- ❌ 渐变背景

### 2. 推荐的颜色
- ✅ Sky 50-500 各层级
- ✅ 蓝色系 (blue-500, blue-600)
- ✅ 青色系 (cyan-400, cyan-500)

### 3. 卡片选择指南
- **主内容**: bg-sky-100 bg-opacity-50
- **次要信息**: bg-sky-50 bg-opacity-60
- **强调内容**: bg-sky-200 bg-opacity-40
- **高亮内容**: bg-sky-300 bg-opacity-30

### 4. 排版建议
- 标题简洁有力，避免过长
- 正文行高 1.6 保证可读性
- 列表项间距 0.75rem
- 段落间距 1.5rem

## 文件结构

```
chat2agent/
├── slides.md              # 主演示文件
├── slides_en.md           # 英文版演示
└── styles/
    ├── style.css          # 主样式文件
    └── theme.css          # 主题配置文件
```

## 维护建议

1. **保持克制**: 新增组件时遵循极简原则
2. **测试对比**: 确保文字对比度符合 WCAG AA 标准
3. **性能优先**: CSS 选择器避免过深嵌套
4. **一致性**: 所有颜色使用 CSS 变量，便于主题切换

## 常见问题

### Q: 如何更改主题色？
A: 修改 `styles/style.css` 中的 `--slidev-theme-primary` 变量

### Q: 如何调整标题位置？
A: 修改 `styles/theme.css` 中的 `.slidev-layout h1, h2` 选择器

### Q: 如何添加新卡片样式？
A: 在 `styles/theme.css` 中添加新的背景色类，确保使用 Sky Blue 色系

## 版本历史

- **v1.0** (2026-04-26): 初始版本，Light + Sky Blue 极简主题
