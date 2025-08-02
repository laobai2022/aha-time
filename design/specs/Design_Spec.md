# Aha App 设计规范文档 (Design System Specification)

## 项目概述

**项目名称**: Aha - 灵感变现即时操作系统  
**设计版本**: v1.0  
**目标平台**: iOS 移动端应用  
**设计风格**: 暗黑科技主题 + 玻璃拟态  
**技术栈**: HTML5 + Tailwind CSS + FontAwesome  

---

## 设计原则

### 1. 用户体验原则
- **零认知负荷**: 界面文字≤小学六年级阅读水平
- **7天法则**: 新用户从注册到发布首个应用≤7天
- **Aha时刻强化**: 关键操作触发多感官反馈（视觉+听觉+触觉）
- **零代码理念**: 用户全程无代码触及

### 2. 视觉设计原则
- **深度层次**: 利用玻璃拟态和阴影营造空间感
- **动态反馈**: 所有交互元素提供即时视觉反馈
- **数据可视化**: 收益数据实时映射为空间动态效果
- **无障碍设计**: 遵循WCAG 2.1 AAA标准

---

## 色彩系统

### 主色调 (Primary Colors)
```css
/* 品牌主色 */
--primary-cyan: #06b6d4      /* 主要操作、链接 */
--primary-purple: #8b5cf6    /* 次要操作、装饰 */
--primary-gradient: linear-gradient(135deg, #06b6d4, #8b5cf6)

/* 功能色彩 */
--success-green: #10b981     /* 成功状态、收益 */
--warning-orange: #f59e0b    /* 警告、付费 */
--error-red: #ef4444         /* 错误、危险操作 */
--info-blue: #3b82f6         /* 信息提示 */
```

### 中性色 (Neutral Colors)
```css
/* 背景色 */
--bg-primary: #0a0a0a        /* 主背景 */
--bg-secondary: #1a1a2e      /* 次要背景 */
--bg-tertiary: #16213e       /* 第三层背景 */

/* 文字色 */
--text-primary: #ffffff      /* 主要文字 */
--text-secondary: #e5e7eb    /* 次要文字 */
--text-tertiary: #9ca3af     /* 辅助文字 */
--text-quaternary: #6b7280   /* 占位符文字 */
```

### 玻璃拟态色彩
```css
/* 玻璃效果 */
--glass-bg: rgba(255, 255, 255, 0.05)
--glass-border: rgba(255, 255, 255, 0.1)
--glass-hover: rgba(255, 255, 255, 0.08)

/* 霓虹发光 */
--neon-cyan: rgba(6, 182, 212, 0.3)
--neon-purple: rgba(139, 92, 246, 0.3)
```

---

## 字体系统

### 字体族
- **主字体**: SF Pro Display (iOS系统字体)
- **备用字体**: system-ui, -apple-system, sans-serif

### 字体大小规范
```css
/* 标题字体 */
--text-5xl: 3rem      /* 48px - 主标题 */
--text-4xl: 2.25rem   /* 36px - 二级标题 */
--text-3xl: 1.875rem  /* 30px - 三级标题 */
--text-2xl: 1.5rem    /* 24px - 四级标题 */
--text-xl: 1.25rem    /* 20px - 五级标题 */

/* 正文字体 */
--text-lg: 1.125rem   /* 18px - 大正文 */
--text-base: 1rem     /* 16px - 标准正文 */
--text-sm: 0.875rem   /* 14px - 小正文 */
--text-xs: 0.75rem    /* 12px - 辅助文字 */
```

### 字重规范
- **Light (300)**: 装饰性文字
- **Regular (400)**: 正文内容
- **Medium (500)**: 次要标题
- **SemiBold (600)**: 重要信息
- **Bold (700)**: 主要标题

---

## 间距系统

### 基础间距单位
基于 4px 网格系统：
```css
--space-1: 0.25rem    /* 4px */
--space-2: 0.5rem     /* 8px */
--space-3: 0.75rem    /* 12px */
--space-4: 1rem       /* 16px */
--space-5: 1.25rem    /* 20px */
--space-6: 1.5rem     /* 24px */
--space-8: 2rem       /* 32px */
--space-10: 2.5rem    /* 40px */
--space-12: 3rem      /* 48px */
--space-16: 4rem      /* 64px */
--space-20: 5rem      /* 80px */
```

### 组件内边距
- **小组件**: 12px (space-3)
- **中等组件**: 16px (space-4)
- **大组件**: 24px (space-6)
- **页面容器**: 24px (space-6)

---

## 圆角系统

```css
--rounded-sm: 0.125rem    /* 2px - 小元素 */
--rounded: 0.25rem        /* 4px - 按钮、输入框 */
--rounded-md: 0.375rem    /* 6px - 卡片边缘 */
--rounded-lg: 0.5rem      /* 8px - 大卡片 */
--rounded-xl: 0.75rem     /* 12px - 模态框 */
--rounded-2xl: 1rem       /* 16px - 主要容器 */
--rounded-3xl: 1.5rem     /* 24px - 特殊容器 */
--rounded-full: 50%       /* 圆形元素 */
```

---

## 阴影系统

### 层级阴影
```css
/* 基础阴影 */
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05)
--shadow: 0 1px 3px rgba(0, 0, 0, 0.1)
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1)
--shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1)
--shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.1)
--shadow-2xl: 0 25px 50px rgba(0, 0, 0, 0.25)

/* 设备阴影 */
--device-shadow: 0 25px 50px rgba(0, 0, 0, 0.5)
--device-shadow-hover: 0 30px 60px rgba(0, 255, 255, 0.2)

/* 霓虹发光 */
--neon-glow: 0 0 20px rgba(0, 255, 255, 0.3)
--neon-glow-strong: 0 0 30px rgba(0, 255, 255, 0.5)
```

---

## 组件库

### 1. 按钮组件

#### 主要按钮 (Primary Button)
```css
.btn-primary {
  background: linear-gradient(90deg, #06b6d4, #8b5cf6);
  color: white;
  padding: 12px 24px;
  border-radius: 16px;
  font-weight: 600;
  box-shadow: 0 0 20px rgba(0, 255, 255, 0.3);
  transition: all 0.3s ease;
}

.btn-primary:hover {
  transform: scale(1.05);
  box-shadow: 0 0 25px rgba(0, 255, 255, 0.4);
}
```

#### 次要按钮 (Secondary Button)
```css
.btn-secondary {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  color: white;
  padding: 12px 24px;
  border-radius: 16px;
  backdrop-filter: blur(20px);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.08);
}
```

### 2. 输入框组件

```css
.input-field {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 16px;
  color: white;
  backdrop-filter: blur(20px);
}

.input-field:focus {
  border-color: rgba(0, 255, 255, 0.5);
  box-shadow: 0 0 20px rgba(0, 255, 255, 0.2);
  outline: none;
}
```

### 3. 卡片组件

```css
.card-glass {
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 16px;
  padding: 24px;
  backdrop-filter: blur(20px);
  transition: all 0.3s ease;
}

.card-glass:hover {
  background: rgba(255, 255, 255, 0.08);
  transform: translateY(-5px);
}
```

### 4. 设备框架组件

```css
.device-frame {
  width: 375px;
  height: 812px;
  background: #000;
  border-radius: 45px;
  padding: 8px;
  box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
  position: relative;
}

.device-screen {
  width: 100%;
  height: 100%;
  border-radius: 37px;
  overflow: hidden;
  background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
}

.status-bar {
  height: 44px;
  background: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 50;
}

.home-indicator {
  width: 134px;
  height: 5px;
  background: rgba(255, 255, 255, 0.6);
  border-radius: 3px;
  position: absolute;
  bottom: 8px;
  left: 50%;
  transform: translateX(-50%);
}
```

---

## 动画与交互

### 1. 过渡动画
```css
/* 标准过渡 */
.transition-standard {
  transition: all 0.3s ease;
}

/* 快速过渡 */
.transition-fast {
  transition: all 0.15s ease;
}

/* 慢速过渡 */
.transition-slow {
  transition: all 0.5s ease;
}
```

### 2. 关键帧动画

#### 浮动效果
```css
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.floating {
  animation: float 3s ease-in-out infinite;
}
```

#### 脉冲效果
```css
@keyframes pulse {
  0%, 100% { opacity: 0.7; transform: scale(1); }
  50% { opacity: 1; transform: scale(1.05); }
}

.pulse {
  animation: pulse 2s infinite;
}
```

#### 发光效果
```css
@keyframes glow {
  0%, 100% { box-shadow: 0 0 20px rgba(0, 255, 255, 0.3); }
  50% { box-shadow: 0 0 30px rgba(0, 255, 255, 0.6); }
}

.glow {
  animation: glow 2s ease-in-out infinite;
}
```

### 3. 涟漪效果 (Ripple Effect)
```javascript
// 为按钮添加涟漪效果的通用函数
function addRippleEffect(element, event) {
  const ripple = document.createElement('div');
  const rect = element.getBoundingClientRect();
  const size = Math.max(rect.height, rect.width);
  const x = event.clientX - rect.left - size / 2;
  const y = event.clientY - rect.top - size / 2;
  
  ripple.style.cssText = `
    position: absolute;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.3);
    transform: scale(0);
    animation: ripple 0.6s linear;
    width: ${size}px;
    height: ${size}px;
    left: ${x}px;
    top: ${y}px;
  `;
  
  element.style.position = 'relative';
  element.style.overflow = 'hidden';
  element.appendChild(ripple);
  
  setTimeout(() => ripple.remove(), 600);
}
```

---

## 图标系统

### 图标库
**主要图标库**: FontAwesome 6.5.1
**CDN链接**: `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css`

### 图标尺寸规范
```css
--icon-xs: 0.75rem     /* 12px */
--icon-sm: 0.875rem    /* 14px */
--icon-base: 1rem      /* 16px */
--icon-lg: 1.125rem    /* 18px */
--icon-xl: 1.25rem     /* 20px */
--icon-2xl: 1.5rem     /* 24px */
--icon-3xl: 1.875rem   /* 30px */
--icon-4xl: 2.25rem    /* 36px */
```

### 核心图标映射
- **品牌图标**: `fas fa-lightbulb` (灵感灯泡)
- **登录**: `fas fa-rocket` (火箭)
- **灵感**: `fas fa-magic` (魔法棒)
- **构建**: `fas fa-tools` (工具)
- **空间**: `fas fa-cube` (立方体)
- **收益**: `fas fa-chart-line` (图表)
- **广场**: `fas fa-store` (商店)
- **个人**: `fas fa-user-circle` (用户)
- **代币**: `fas fa-coins` (代币)

---

## 响应式设计

### 断点系统
```css
/* 移动端优先 */
@media (min-width: 640px) { /* sm */ }
@media (min-width: 768px) { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1280px) { /* xl */ }
@media (min-width: 1536px) { /* 2xl */ }
```

### 设备适配
- **主要目标**: iPhone 14 Pro (375×812px)
- **兼容设备**: iPhone 12/13/14 系列
- **最小支持**: iPhone SE (375×667px)

---

## 无障碍设计

### 1. 颜色对比度
- **文字对比度**: 至少 4.5:1 (WCAG AA)
- **大文字对比度**: 至少 3:1 (WCAG AA)
- **UI元素对比度**: 至少 3:1

### 2. 交互元素
- **最小点击区域**: 44×44px (符合Apple HIG)
- **键盘导航**: 支持Tab键遍历
- **焦点状态**: 明显的焦点指示器

### 3. 语音辅助
- **全图标语音标签**: 点击朗读功能描述
- **语音控制**: 支持"保存灵感"、"发布应用"等指令
- **头部姿态识别**: 通过摄像头点头确认操作

---

## 性能优化

### 1. 资源加载
- **图片优化**: 使用WebP格式，渐进式加载
- **字体优化**: 字体预加载，fallback字体
- **CSS优化**: 关键CSS内联，非关键CSS异步加载

### 2. 动画性能
- **硬件加速**: 使用transform和opacity属性
- **避免重排**: 不改变布局的动画
- **帧率控制**: 保持60fps流畅度

---

## 开发规范

### 1. CSS类命名
遵循BEM命名约定：
```css
/* Block__Element--Modifier */
.card { }
.card__header { }
.card__header--highlighted { }
```

### 2. 组件结构
```html
<!-- 标准组件结构 -->
<div class="component-name">
  <header class="component-name__header">
    <!-- 头部内容 -->
  </header>
  <main class="component-name__content">
    <!-- 主要内容 -->
  </main>
  <footer class="component-name__footer">
    <!-- 底部内容 -->
  </footer>
</div>
```

### 3. 注释规范
```css
/* ==========================================================================
   组件名称
   ========================================================================== */

/**
 * 组件说明
 * 1. 设计要点说明
 * 2. 使用场景说明
 */
.component {
  /* 具体样式 */
}
```

---

## 设计资源

### 1. 设计工具
- **原型工具**: 直接使用HTML/CSS实现
- **图标资源**: FontAwesome
- **图片资源**: Unsplash, Pexels
- **字体资源**: Apple系统字体

### 2. 颜色工具
- **色彩搭配**: Adobe Color, Coolors.co
- **对比度检测**: WebAIM Contrast Checker
- **调色板生成**: Material Design Color Tool

### 3. 参考资源
- **设计规范**: Apple Human Interface Guidelines
- **交互模式**: iOS Human Interface Guidelines
- **可访问性**: WCAG 2.1 Guidelines

---

## 版本历史

### v1.0 (当前版本)
- ✅ 完成基础色彩系统
- ✅ 建立字体规范
- ✅ 实现玻璃拟态效果
- ✅ 完成核心组件库
- ✅ 实现设备框架模拟
- ✅ 添加动画交互系统
- ✅ 优化无障碍设计

### 未来计划
- 🔄 多语言支持
- 🔄 深色/浅色主题切换
- 🔄 自定义主题系统
- 🔄 更多动画效果
- 🔄 高级交互组件

---

*本设计规范文档将随项目发展持续更新和完善。* 