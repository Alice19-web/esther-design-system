# App 型 / 功能型页面设计规范

适用于：

* 个人看板 Dashboard
* 数字书架 Library
* Canvas 无限画布
* 知识管理系统
* Obsidian 类应用
* AI 工作台
* 数据后台

核心定位：

> 功能优先，视觉克制，交互清晰。

---

# 核心原则

## 1. 功能优先

装饰元素最少化。

页面首先服务于操作效率，而非视觉展示。

避免：

* 大面积装饰插画
* 无意义渐变
* 复杂背景纹理
* 强干扰动画

---

## 2. 信息密度适中

App 页面不是 Landing Page。

允许更高的信息密度：

* 更紧凑间距
* 更高内容承载量
* 更快浏览效率

---

## 3. 交互反馈明确

所有可操作元素必须存在：

* Hover
* Active
* Focus
* Disabled

状态反馈。

---

## 4. 导航永远可见

用户任何时刻都应知道：

* 我在哪里
* 可以去哪里

优先：

* Sticky Header
* Sticky Tab
* Fixed Sidebar

---

# 页面结构

## 标准布局

```text
Sticky Header
      ↓

Tab Bar / Sidebar
      ↓

Main Content
      ↓

Cards / Grid / Canvas
```

---

# Header

高度：

```css
48px ~ 64px
```

推荐：

```css
56px
```

```css
.app-header {
  position: sticky;
  top: 0;
  z-index: 100;

  height: 56px;

  display: flex;
  align-items: center;

  padding: 0 1.5rem;

  background: var(--cream, #fefcf6);

  border-bottom: 1px solid rgba(26,26,26,.06);
}
```

---

# Sidebar

适用于：

* 知识库
* 书架
* 工作台
* Canvas

```css
.app-sidebar {
  position: fixed;

  top: 56px;
  left: 0;
  bottom: 0;

  width: 220px;

  padding: 1.5rem 1rem;

  overflow-y: auto;

  border-right: 1px solid rgba(26,26,26,.06);
}
```

---

# Main Area

```css
.app-main {
  margin-left: 220px;

  padding: 2rem;

  max-width: 1200px;
}
```

---

# Content Area

标准阅读区：

```css
.app-content {
  max-width: 820px;

  margin: 0 auto;

  padding: 2rem 1.5rem;
}
```

---

宽布局：

```css
.app-content--wide {
  max-width: 1200px;
}
```

适用于：

* Dashboard
* 看板
* 瀑布流
* 书架

---

# 色彩系统

## 页面背景

```css
#fefcf6
```

品牌暖白底。

---

## 卡片背景

```css
#ffffff
```

白卡片浮于暖色背景。

---

## 主交互色

```css
var(--blue)
```

推荐：

```css
#4A7CC9
```

用于：

* Header
* Active Tab
* 按钮
* 链接

---

## 强调色

```css
var(--yellow)
```

推荐：

```css
#E8B84A
```

用于：

* Badge
* 标签
* 边框强调

---

## 危险色

```css
var(--red)
```

推荐：

```css
#C65A46
```

仅用于：

* 删除
* 警告
* 不可逆操作

---

## 特殊功能色

绿色板块：

```css
#2D6A4F
```

用于：

* 梦境系统
* 自然模块
* 森林类内容

---

# 分类标签扩展色

允许增加：

* 蓝
* 黄
* 绿
* 红
* 灰
* 棕

总色板控制：

```text
≤ 6种
```

要求：

```text
低饱和度
低对比
统一品牌气质
```

---

# Tab 导航

```css
.tab-bar {
  display: flex;

  gap: 4px;

  overflow-x: auto;

  border-bottom: 2px solid #eee;
}
```

```css
.tab {
  padding: 10px 20px;

  border: none;

  background: transparent;

  cursor: pointer;

  font-size: .9rem;

  border-bottom: 2px solid transparent;

  margin-bottom: -2px;

  transition: all .2s;
}
```

```css
.tab.active {
  color: var(--blue);

  border-bottom-color: var(--blue);

  font-weight: 600;
}
```

---

# Modal

```css
.modal-overlay {
  position: fixed;

  inset: 0;

  z-index: 1000;

  background: rgba(0,0,0,.6);

  backdrop-filter: blur(4px);

  display: flex;

  align-items: center;

  justify-content: center;
}
```

```css
.modal-content {
  width: 90%;

  max-width: 560px;

  max-height: 80vh;

  overflow-y: auto;

  padding: clamp(24px,3vw,40px);

  border-radius: 16px;

  background: var(--cream,#fefcf6);
}
```

---

# 卡片系统

## 标准卡片

```css
.app-card {
  background: #fff;

  border-radius: 12px;

  padding: 1.25rem;

  cursor: pointer;

  box-shadow: 0 2px 12px rgba(0,0,0,.04);

  transition:
    transform .2s,
    box-shadow .2s;
}
```

---

## Hover

```css
.app-card:hover {
  transform: translateY(-2px);

  box-shadow: 0 8px 24px rgba(0,0,0,.08);
}
```

---

# 输入框

```css
.app-input {
  background: #fff;

  border-radius: 8px;

  padding: 10px 14px;

  font-size: .9rem;

  border: 1.5px solid rgba(26,26,26,.1);

  transition: border-color .2s;
}
```

---

## Focus

```css
.app-input:focus {
  outline: none;

  border-color: var(--blue,#4A7CC9);

  box-shadow:
    0 0 0 3px rgba(74,124,201,.10);
}
```

---

# 无限画布 Canvas

适用于：

* 白板
* 思维导图
* 卡片关系图
* 灵感墙

---

## Grid Dot 背景

```css
.canvas-grid {
  width: 100%;
  height: 100%;

  background-image:
  radial-gradient(
    circle,
    rgba(74,124,201,.13) 1.2px,
    transparent 1.2px
  );

  background-size: 28px 28px;
}
```

---

## Cursor

```css
.canvas-area {
  cursor: grab;
}

.canvas-area:active {
  cursor: grabbing;
}
```

---

## Transform Layer

```css
.canvas-transform {
  position: absolute;

  transform-origin: 0 0;

  will-change: transform;
}
```

---

## Canvas Card

手绘感卡片。

```css
.canvas-card {
  background: #fff;

  border-radius: 16px;

  padding: 1.25rem;

  border: 2px dashed rgba(74,124,201,.35);

  box-shadow:
    0 4px 16px rgba(0,0,0,.06);
}
```

---

# 响应式

## Header

保持高度。

缩减：

* Logo
* 搜索框
* 辅助操作

---

## Sidebar

桌面端：

```text
固定侧边栏
```

移动端：

```text
Bottom Tab
或
Hamburger Menu
```

---

## Grid

统一：

```css
grid-template-columns:
repeat(
auto-fill,
minmax(260px,1fr)
);
```

---

## Modal

桌面：

```text
居中弹窗
```

移动：

```text
全屏
或
Bottom Sheet
```

---

# 动效规范

允许：

* Hover
* Focus
* Modal
* Dropdown

时长：

```css
200ms
```

---

禁止：

* Scroll Reveal
* 大幅视差
* 页面级动画
* 强打断式过渡

App 页面必须即时响应。

---

# 字体规范

标题：

```css
1rem ~ 1.2rem
```

正文：

```css
0.9rem
```

辅助信息：

```css
0.8rem
```

禁止：

```text
2rem+
超大标题
```

功能页不是杂志排版。

---

# App 页面禁忌

❌ 大段装饰性文案

❌ Hero Banner

❌ Landing Page布局

❌ Scroll Reveal动画

❌ 深色内容面板

❌ 高饱和渐变

❌ 超大标题

❌ 炫技式交互

❌ 无意义玻璃拟态

---

# 最终设计目标

视觉感受：

```text
像 Notion 一样清爽

像 Obsidian 一样高效

像 Linear 一样克制

像 Apple Notes 一样易用
```

品牌气质：

```text
温暖
理性
安静
高级
可长期使用
```

核心原则：

功能优先 > 内容优先 > 视觉优先
