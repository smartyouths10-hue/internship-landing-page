# 🚀 马来西亚保险 Agency 招募 Landing Page 策划方案 (Project Readme)

本方案基于 **“温润、专业、高透明度”** 的视觉风格（参考原图：沐尼白木耳设计），旨在为马来西亚保险代理团队打造一个极具亲和力、告别“硬推销感”的高转化率招募页面。

---

## 🎨 视觉设计规范 (Design System)

### 1. 色彩规范 (Color Palette)
| 角色 | 十六进制 (HEX) | 视觉感官 | 备注 |
| :--- | :--- | :--- | :--- |
| **主背景色** | `#F9F7F2` | 米白色 | 模拟有机质感，消除数码冰冷感 |
| **次要背景** | `#F2EDE4` | 浅木色 | 用于 Section 切换，产生视觉节奏 |
| **品牌主色** | `#7D6348` | 深木色 | 用于大标题，代表稳重与专业 |
| **行动触发 (CTA)** | `#D4A373` | 温暖金 | 用于按钮、Checklist、核心亮点 |
| **正文颜色** | `#4A4A4A` | 深灰色 | 确保阅读清晰度，不使用纯黑 |

### 2. 字体与排版 (Typography)
* **标题 (H1, H2):** 建议使用现代无衬线粗体（如 *PingFang SC Semibold*），字间距设定为 `2px`。
* **副标题:** 建议使用细体宋体或楷体，营造一种“生活提案”的感性氛围。
* **圆角与留白:** 统一使用 `12px` 圆角。Section 上下 Padding 保持在 `80px` (PC) / `40px` (Mobile)。

---

## 🏗️ 页面结构策划 (Content Strategy)

### Section 1: 视觉首屏 (Hero Section)
* **布局:** 左右/居中对齐，背景使用高质感团队合照（Business Casual 风格）。
* **主标题:** 重新定义你的事业：在马来西亚，开启一份“有温度”的高薪事业。
* **副标题:** [Agency Name] 招募合伙人：从平凡到卓越，我们陪你走每一步。

### Section 2: 痛点解析 (The Pain Points) - *对应原图圆圈布局*
* **视觉:** 3-4 个圆形边框图标。
* **核心内容:** 针对马来西亚职场现状（如：塞车时间长、薪水追不上通胀、缺乏职业安全感）。

### Section 3: 核心优势 (Our Values) - *对应原图 Checklist 布局*
* **布局:** 左侧真实照片，右侧 Checklist。
* **文案亮点:** 强调“独家引流系统”、“MDRT 导师制”、“家庭事业平衡”。

### Section 4: 竞争对比 (The PK Table) - *对应原图底部 PK 布局*
* **布局:** 深浅双色色块对比表。
* **逻辑:** 传统行业（收入封顶、办公室政治） vs. [Agency]（透明晋升、共享资源、像家人的团队）。

### Section 5: 成长路径 (Growth Map)
* **视觉:** 阶梯式递进图示。
* **阶段:** * 1-3月：新人实战营（专业起步）
    * 4-6月：个人品牌建立（业绩爆发）
    * 7-12月：管理层培育（团队领袖）

### Section 6: 真实见证 (Testimonials)
* **视觉:** 引用人物真实语录，配以工作场景照。

---

## 💻 核心代码框架 (CSS Implementation)

### 响应式布局核心
```css
:root {
  --bg-primary: #F9F7F2;
  --primary-color: #7D6348;
  --accent-color: #D4A373;
}

/* 基础 Section 样式 */
.section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 80px 20px;
  display: flex;
  align-items: center;
  gap: 50px;
}

/* 手机端适配逻辑 */
@media (max-width: 768px) {
  .section {
    flex-direction: column !important; /* 强制垂直堆叠 */
    text-align: center;
    padding: 40px 15px;
  }
  .image-container {
    width: 100%;
    order: -1; /* 图片居上 */
  }
}

/* 模仿原图的圆圈列表 */
.circle-item {
  width: 150px;
  height: 150px;
  border: 1px dashed var(--accent-color);
  border-radius: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  background: #fff;
}