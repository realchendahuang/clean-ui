# 克制设计 · Clean UI

> 全球化独立产品审美与克制设计手册：排版、色彩与极简交互  
> Minimalist design principles, typography, palette & UI recipes for indie builders.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/realchendahuang/clean-ui/pulls)

---

## 设立宗旨

很多独立产品功能十分硬核，但第一眼往往被用户关闭，根源在于界面缺乏审美克制感：元素拥挤排布、五颜六色、充满死板的大厂后台公文感。

克制设计（Clean UI）致力于为独立产品交付一套极简、耐看、国际化的设计规范：
1. 留白与呼吸感：以负空间为第一公民，严格统一组件间距阶梯；
2. 色彩克制：以黑白深灰为骨架底色，全站至多保留一种功能性高饱和强调色；
3. 即拷即用代码片段：Tailwind CSS 极简预设、细腻微动效与骨架屏实现。

---

## 极简设计核心原则

### 1. 字体层级与行高
- **字号阶梯**：全站严格控制在 4 个字阶以内（标题 20/24px、二级标题 16px、正文 14px、辅助标注 12px）；
- **行高比例**：正文行高保持在 1.6 到 1.8 之间，确保长文本阅读舒适无压迫感；
- **字重节制**：只有真正需要强调的主标题才用 Medium 或 SemiBold，正文坚决不滥用加粗。

### 2. 灰阶与色彩体系
- **暗黑模式背景**：不要使用纯黑（#000000），使用带极微弱暖调的深灰（如 #0a0a0a 或 #121212），避免对比度过高刺眼；
- **边框与分割线**：边框颜色采用半透明白色叠加（如 border-white/10 或 border-white/5），让层次感自然柔和；
- **强调色原则**：主操作按钮采用高对比度单色（如纯白按钮配黑字），状态指示采用纯正绿/琥珀色/红。

### 3. 微动效分寸感
- **动画时长**：悬浮过渡与展开动画严格控制在 150ms 到 200ms 之内，杜绝拖泥带水；
- **缓动函数**：统一采用 cubic-bezier(0.16, 1, 0.3, 1) 带来类似原生 macOS 的清脆回弹；
- **无感骨架屏**：数据加载阶段使用低对比度微光扫描动画，防止页面产生突兀跳变。

---

## Tailwind CSS 极简预设片段

```js
// tailwind.config.js 推荐极简配置片段
module.exports = {
  darkMode: 'class',
  theme: {
    extend: {
      colors: {
        canvas: {
          light: '#ffffff',
          dark: '#09090b',
        },
        surface: {
          light: '#f4f4f5',
          dark: '#18181b',
        },
        border: {
          light: '#e4e4e7',
          dark: '#27272a',
        }
      }
    }
  }
}
```

---

## 上线前自查清单（Checklist）

- [ ] 页面在移动端竖屏状态下，首屏核心信息与操作按钮是否一眼可见？
- [ ] 页面所有不可点击的文字是否完全杜绝了类似链接的下划线与误导色？
- [ ] 弹窗与悬浮菜单是否支持 Escape 键一键退出？
- [ ] 表单输入框是否具有清晰的 Focus 环与清脆的原生交互反馈？

---

## License

MIT License. Copyright (c) 2026 realchendahuang.
