---

name: mingyue-design-system
description: 明月Moon设计系统。用于个人品牌网站、知识库、作品集、AI产品、活动页、教程页、小红书图文等内容的统一设计语言。
----------------------------------------------------------------------

# 明月Moon Design System

适用于：

* 个人品牌网站
* 作品集网站
* AI产品页面
* Obsidian知识库
* 教程页面
* 科普页面
* Landing Page
* 活动页
* 小红书图文
* 图文卡片
* 内容资产设计

---

# 设计系统优先级

严格按照以下顺序执行：

```text
brand-dna.md
↓
scene-*.md
↓
components.md
↓
layouts.md
↓
checklist.md
```

如发生冲突：

```text
brand-dna.md 永远优先
```

禁止：

* 新建品牌色
* 新建字体体系
* 新建设计语言
* 新建动效体系

所有页面必须继承品牌DNA。

---

# 触发条件

当用户要求：

* 制作HTML页面
* 制作网页
* 制作教程页
* 制作介绍页
* 制作活动页
* 制作Landing Page
* 制作个人网站
* 制作作品集
* 制作App页面
* 制作Canvas页面
* 制作知识库页面
* 制作图文卡片
* 制作小红书图文
* 文章转图文
* 做卡片
* 内容可视化

时自动触发。

---

# 使用方式（7步工作流）

## Step 1：澄清需求

向用户确认：

### 1. 页面类型

* 教程型
* 介绍型
* 科普型
* Landing Page
* 活动页
* App页面
* 图文卡片
* 作品集页面
* 个人品牌页面

### 2. 使用场景

* 明月Moon
* 无尘阁
* AI实验室
* Obsidian知识库
* 小红书
* 公众号
* 个人网站

### 3. 受众

给谁看？

技术水平如何？

### 4. 内容规模

大约几屏内容？

### 5. 素材

是否已有：

* 文案
* 图片
* 数据
* 视频

### 6. 硬约束

必须包含什么？

是否存在合作品牌色？

---

## Step 2：读取规范

### 必读

```text
brand-dna.md
```

确认：

* 品牌气质
* 色彩体系
* 字体体系
* 禁忌清单

---

### 根据场景读取

教程型 / 介绍型 / 科普型：

```text
references/scene-tutorial.md
```

活动页 / 分享会 / Landing：

```text
references/scene-landing.md
```

App型 / 功能型：

```text
references/scene-app.md
```

图文卡片 / 小红书图文：

```text
references/scene-cards.md
```

---

## Step 3：选择模板

从 assets 选择对应模板。

教程型：

```text
assets/template-tutorial.html
```

Landing：

```text
assets/template-landing.html
```

App：

```text
assets/template-app.html
```

图文卡片：

```text
assets/template-cards.html
```

原则：

```text
从模板开始修改
不要从零开始写
```

---

## Step 4：选择布局

从：

```text
references/layouts.md
```

选择：

```text
3~5种布局模式
```

要求：

```text
每个Section布局必须不同
```

避免：

```text
重复排列
机械堆叠
```

图文卡片模式：

参考：

```text
scene-cards.md
```

中的推荐排版方式。

---

## Step 5：选择组件

从：

```text
references/components.md
```

选择组件填充内容。

硬规则：

禁止浏览器默认样式。

不允许：

* 默认blockquote
* 默认table
* 默认ul
* 默认ol
* 默认引用块

所有组件必须：

* 来自components.md
* 或按照brand-dna规范重新设计

---

## Step 6：质量检查

对照：

```text
references/checklist.md
```

逐条检查。

### P0

必须全部通过。

任何一项失败：

```text
直接返工
```

### P1

尽量通过。

### P2

作为加分项。

图文模式：

额外检查：

```text
scene-cards.md
```

中的Checklist。

---

## Step 7：交付

输出：

* HTML
* CSS
* React组件
* Next.js页面

确保：

```text
可直接运行
可直接部署
```

---

# 场景速查

| 类型          | 场景文件              | 模板                     |
| ----------- | ----------------- | ---------------------- |
| 教程型/介绍型/科普型 | scene-tutorial.md | template-tutorial.html |
| 活动页/Landing | scene-landing.md  | template-landing.html  |
| App页面       | scene-app.md      | template-app.html      |
| 图文卡片/小红书图文  | scene-cards.md    | template-cards.html    |

---

# 核心原则

## 品牌一致性优先

所有设计必须继承：

```text
brand-dna.md
```

禁止创造新的：

* 品牌色
* 字体体系
* 动效体系
* 装饰语言

---

## 模板优先

原则：

```text
从模板开始改
不要从零开始写
```

---

## 布局多样性

要求：

```text
每个Section布局不同
```

避免：

```text
连续重复布局
```

---

## 完成必须检查

交付前：

```text
必须通过checklist
```

---

# 品牌目标

最终输出应符合：

* 东方现代主义
* 出版物美学
* 艺术馆气质
* 禅意设计
* 知识型品牌

---

# 品牌关键词

```text
温暖

克制

理性

高级

留白

长期主义

安静

东方
```

---

# 禁止风格

```text
科技感

赛博朋克

互联网大厂风

运营海报风

AI模板风

高饱和渐变

Neon

Cyan

蓝紫渐变

炫技式动画
```

---

# 最终判断标准

生成结果应该像：

```text
一本优秀的设计出版物
一座现代艺术馆
一个长期运营的个人品牌
```

而不是：

```text
互联网产品官网
营销活动海报
AI自动生成模板
```
