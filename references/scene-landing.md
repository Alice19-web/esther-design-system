# Landing Page / 活动页 / 分享会页面设计规范

适用于：

* 分享会邀请页
* 活动报名页
* 产品发布页
* 品牌合作宣传页
* AI产品介绍页
* 个人IP活动页
* MOON明月主题活动页

核心定位：

> 强节奏、高转化、高情绪价值。

通过视觉节奏与内容结构推动用户完成行动。

---

# 核心原则

## 1. 更大的 Hero

首屏必须建立情绪。

推荐：

```css
min-height: 100vh;
```

目标：

* 一眼知道主题
* 一眼知道价值
* 一眼知道下一步

---

## 2. 更强的节奏感

Landing Page不是文档页。

必须通过：

* 深浅面板交替
* 图片与文字交替
* 卡片与引用交替

制造阅读节奏。

---

## 3. 深色面板必须出现

每个Landing Page：

至少包含：

```text
1~2个全宽深色面板
```

用于：

* 金句
* 核心观点
* 品牌宣言
* 重要数据

---

## 4. CTA持续出现

用户不应阅读到最后才知道如何行动。

推荐：

```text
Hero CTA
↓

中段 CTA

↓

最终 CTA
```

每个逻辑段结束后都应存在下一步引导。

---

## 5. 情绪递进

标准结构：

```text
痛点
 ↓

认知
 ↓

方案
 ↓

证据
 ↓

信任
 ↓

行动
```

不要直接卖产品。

先建立认同。

---

# 页面结构

推荐节奏：

```text
Hero（全屏）
     ↓

三列价值卡片
     ↓

深色品牌面板
     ↓

内容介绍区
     ↓

时间线 / 流程图
     ↓

嘉宾 / 案例
     ↓

Pull Quote
     ↓

CTA行动区
```

---

# Hero 区域

## 推荐形式

### 方案A

单栏纵向

```text
Logo

标题

副标题

CTA
```

适用于：

* 分享会
* 发布会
* 个人IP

---

### 方案B

双栏不对称

```text
左：
标题 + CTA

右：
视觉主图
```

适用于：

* 产品发布
* 品牌合作
* SaaS Landing

---

## Hero规范

```css
.hero {
  min-height: 100vh;

  display: flex;
  align-items: center;

  padding:
  clamp(40px,8vw,120px);
}
```

---

# 色彩系统

继承：

```text
brand-dna.md
```

三色体系。

---

# 合作品牌扩展色

仅当涉及合作品牌时使用。

---

## Cola合作

```css
#F1752D
```

用途：

* CTA强调
* 数据高亮
* 重点标签

替代：

```text
红色强调位
```

---

## 金橙色

```css
#F7A946
```

适用于：

* 时间信息
* Slogan
* 活动日期

---

# 使用规则

第四色：

```text
只能替代红色位置
```

禁止：

```text
替代品牌蓝
替代品牌黄
```

---

# 深色面板

## 标准深色

```css
#151821
```

---

## 极深色

```css
#0D1117
```

---

## 品牌蓝面板

```css
background: var(--blue);
color: white;
```

---

## 品牌黄面板

```css
background: var(--yellow);
color: var(--ink);
```

---

# 布局系统

## Hero

优先级：

```text
单栏纵向
＞
双栏不对称
＞
标准双栏
```

---

## 中部内容

必须通过：

```text
浅色
↓
深色
↓
浅色
↓
深色
```

建立视觉呼吸感。

---

# 三列价值卡片

推荐：

```css
grid-template-columns:
repeat(3,1fr);
```

内容：

* 核心价值
* 嘉宾亮点
* 活动特色

---

# Sticky时间线

适用于：

* 活动流程
* 课程安排
* 产品路线图

结构：

```text
时间
｜
内容
｜
行动
```

---

# Pull Quote

用于：

* 嘉宾金句
* 品牌宣言
* MOON明月核心观点

推荐样式：

```text
“好的设计，
不是制造噪音，
而是创造秩序。”
```

---

# Flow Arrow

适用于：

* 产品流程
* 活动流程
* 用户路径

示例：

```text
报名
 →
确认
 →
参与
 →
复盘
```

---

# Avatar Cluster

适用于：

* 嘉宾展示
* 团队展示
* 合作伙伴展示

推荐：

```text
4~12个头像
```

形成视觉聚焦。

---

# Do / Don't

适用于：

* 用户痛点
* 产品对比
* 认知升级

示例：

```text
DON'T

盲目堆功能
追求复杂交互

DO

聚焦核心体验
建立清晰路径
```

---

# CTA按钮

## 标准按钮

```css
.cta-button {

  display: inline-flex;

  align-items: center;

  gap: 8px;

  padding: 16px 36px;

  border-radius: 12px;

  text-decoration: none;

  font-weight: 600;

  font-size: 1rem;

  background:
  var(--blue,#2F4156);

  color: white;

  transition:
  transform .2s,
  box-shadow .2s;
}
```

---

## Hover

```css
.cta-button:hover {

  transform:
  translateY(-2px);

  box-shadow:
  0 8px 24px
  rgba(47,65,86,.3);
}
```

---

## 黄色按钮

用于：

* 深色背景
* 品牌强调

```css
.cta-button--yellow {

  background:
  var(--yellow,#B89B6C);

  color:
  var(--ink,#1A1A2E);
}
```

---

# CTA区域

```css
.cta-section {

  text-align: center;

  padding:
  clamp(80px,12vh,160px)
  2rem;
}
```

---

## 标题

```css
.cta-section h2 {

  font-family:
  "Noto Serif SC", serif;

  font-size:
  clamp(
    1.6rem,
    4vw,
    2.6rem
  );

  margin-bottom: 1rem;
}
```

---

## 描述

```css
.cta-section p {

  font-size: 1rem;

  color:
  var(--ink-light,#4A4A5A);

  margin-bottom: 2rem;
}
```

---

# 动效系统

Landing允许适度增强。

但必须服务于转化。

---

## 头像轨道旋转

```css
@keyframes heroSpin {

  to {
    transform:
    rotate(360deg);
  }

}

.ring {

  animation:
  heroSpin
  20s
  linear
  infinite;
}
```

---

## 数字递增

适用于：

* 用户数
* 下载量
* 活动人数

推荐：

```text
IntersectionObserver
+
CountUp
```

---

## Stagger Reveal

推荐：

```text
.reveal-d1
.reveal-d2
.reveal-d3
.reveal-d4
.reveal-d5
```

间隔：

```text
0.1s
```

---

# 响应式规范

## Hero

桌面：

```text
双栏
```

移动端：

```text
单栏
```

图片放置：

```text
文字下方
```

---

## 三列卡片

桌面：

```text
3列
```

移动：

```text
1列
```

---

## CTA按钮

移动端：

```css
width: 100%;
```

---

## Pull Quote

移动端：

* 缩小字号
* 缩小Padding

保持阅读舒适。

---

# MOON明月署名规范

适用于：

* 分享会页面
* 个人品牌活动页
* 产品发布页

统一格式：

```text
By MOON明月
```

或

```text
Designed by MOON明月
```

禁止出现：

```text
Admin
Author
Creator
Anonymous
```

统一替换为：

```text
MOON明月
```

---

# Landing Page 禁忌

❌ 品牌蓝底放蓝字

❌ 品牌黄底放黄字

❌ 超过3个CTA按钮

❌ Stock Photo风格图片

❌ 所有Section都是白底

❌ 过长Hero文案

❌ 连续深色面板

❌ 自动轮播Banner

❌ 强制弹窗打断阅读

---

# 最终设计目标

视觉感受：

```text
像 Apple 发布会一样克制

像 Stripe Landing 一样清晰

像 Linear 官网一样高级

像 Notion 活动页一样舒服
```

品牌气质：

```text
温暖

理性

高级

有思想

有节奏
```

核心原则：

情绪优先 ＞ 节奏优先 ＞ 转化优先 ＞ 视觉炫技
