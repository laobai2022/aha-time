# Maxun - Design Specification Document

## 1. 设计概述

### 1.1 设计理念
Maxun 的设计理念是"简单而强大"，通过直观的界面和流畅的用户体验，让复杂的网络数据提取变得简单易用。

### 1.2 设计原则
- **简洁性**: 界面简洁明了，减少认知负担
- **一致性**: 保持设计元素和交互模式的一致性
- **可访问性**: 确保所有用户都能轻松使用
- **响应式**: 适配不同设备和屏幕尺寸
- **现代化**: 采用最新的设计趋势和技术

## 2. 视觉设计规范

### 2.1 色彩系统

#### 主色调
- **主色**: `#6366F1` (Indigo 500) - 用于主要按钮、链接和重要元素
- **辅助色**: `#8B5CF6` (Violet 500) - 用于次要按钮和装饰元素
- **成功色**: `#10B981` (Emerald 500) - 用于成功状态和确认操作
- **警告色**: `#F59E0B` (Amber 500) - 用于警告和提醒
- **错误色**: `#EF4444` (Red 500) - 用于错误状态和危险操作

#### 中性色
- **背景色**: `#0F172A` (Slate 900) - 主背景
- **卡片背景**: `#1E293B` (Slate 800) - 卡片和面板背景
- **边框色**: `#334155` (Slate 700) - 边框和分割线
- **文本主色**: `#F8FAFC` (Slate 50) - 主要文本
- **文本次要色**: `#CBD5E1` (Slate 300) - 次要文本

### 2.2 字体系统

#### 字体族
- **主字体**: Inter - 现代、清晰的无衬线字体
- **代码字体**: JetBrains Mono - 等宽字体，用于代码显示

#### 字体大小
- **标题1**: 2.25rem (36px) - 页面主标题
- **标题2**: 1.875rem (30px) - 区块标题
- **标题3**: 1.5rem (24px) - 子区块标题
- **标题4**: 1.25rem (20px) - 小标题
- **正文**: 1rem (16px) - 主要内容
- **小文本**: 0.875rem (14px) - 辅助信息
- **标签**: 0.75rem (12px) - 标签和注释

#### 字重
- **Light**: 300 - 用于大标题
- **Regular**: 400 - 用于正文
- **Medium**: 500 - 用于强调文本
- **Semibold**: 600 - 用于小标题
- **Bold**: 700 - 用于重要标题

### 2.3 间距系统

#### 基础间距单位
- **4px**: 最小间距单位
- **8px**: 小间距
- **16px**: 标准间距
- **24px**: 中等间距
- **32px**: 大间距
- **48px**: 超大间距

#### 应用规则
- 元素内部间距: 8px-16px
- 元素间间距: 16px-24px
- 区块间间距: 24px-32px
- 页面边距: 16px-24px

### 2.4 圆角系统
- **小圆角**: 4px - 按钮、输入框
- **中圆角**: 8px - 卡片、面板
- **大圆角**: 12px - 模态框、大卡片
- **全圆角**: 50% - 头像、圆形按钮

## 3. 组件设计规范

### 3.1 按钮组件

#### 主要按钮
```css
.btn-primary {
  background: #6366F1;
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.2s;
}

.btn-primary:hover {
  background: #5855EB;
  transform: translateY(-1px);
}
```

#### 次要按钮
```css
.btn-secondary {
  background: transparent;
  color: #6366F1;
  border: 1px solid #6366F1;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 500;
}
```

#### 危险按钮
```css
.btn-danger {
  background: #EF4444;
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 500;
}
```

### 3.2 输入框组件

#### 标准输入框
```css
.input {
  background: #1E293B;
  border: 1px solid #334155;
  color: #F8FAFC;
  padding: 12px 16px;
  border-radius: 8px;
  transition: border-color 0.2s;
}

.input:focus {
  border-color: #6366F1;
  outline: none;
  box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
}
```

### 3.3 卡片组件

#### 标准卡片
```css
.card {
  background: #1E293B;
  border: 1px solid #334155;
  border-radius: 12px;
  padding: 24px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}
```

### 3.4 状态指示器

#### 成功状态
```css
.status-success {
  color: #10B981;
  background: rgba(16, 185, 129, 0.1);
  padding: 4px 8px;
  border-radius: 4px;
}
```

#### 警告状态
```css
.status-warning {
  color: #F59E0B;
  background: rgba(245, 158, 11, 0.1);
  padding: 4px 8px;
  border-radius: 4px;
}
```

#### 错误状态
```css
.status-error {
  color: #EF4444;
  background: rgba(239, 68, 68, 0.1);
  padding: 4px 8px;
  border-radius: 4px;
}
```

## 4. 布局规范

### 4.1 网格系统
- **12列网格**: 用于复杂布局
- **6列网格**: 用于中等复杂度布局
- **4列网格**: 用于简单布局
- **响应式断点**:
  - 移动端: < 768px
  - 平板: 768px - 1024px
  - 桌面: > 1024px

### 4.2 容器宽度
- **最大宽度**: 1200px
- **标准宽度**: 1000px
- **紧凑宽度**: 800px

### 4.3 导航布局
- **顶部导航**: 固定高度 64px
- **侧边栏**: 固定宽度 240px
- **主内容区**: 自适应宽度
- **底部**: 固定高度 60px

## 5. 交互设计规范

### 5.1 动画效果

#### 过渡动画
- **标准过渡**: 0.2s ease-in-out
- **快速过渡**: 0.15s ease-out
- **慢速过渡**: 0.3s ease-in-out

#### 悬停效果
- **按钮悬停**: 轻微上移 + 阴影加深
- **卡片悬停**: 阴影加深 + 轻微缩放
- **链接悬停**: 颜色变化 + 下划线

### 5.2 加载状态

#### 加载指示器
```css
.loading-spinner {
  border: 2px solid #334155;
  border-top: 2px solid #6366F1;
  border-radius: 50%;
  width: 20px;
  height: 20px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

#### 骨架屏
```css
.skeleton {
  background: linear-gradient(90deg, #334155 25%, #475569 50%, #334155 75%);
  background-size: 200% 100%;
  animation: loading 1.5s infinite;
}

@keyframes loading {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}
```

### 5.3 反馈机制

#### 成功反馈
- 绿色状态指示器
- 成功消息提示
- 轻微震动动画

#### 错误反馈
- 红色状态指示器
- 错误消息提示
- 输入框边框变红

#### 警告反馈
- 黄色状态指示器
- 警告消息提示
- 图标闪烁

## 6. 响应式设计

### 6.1 移动端适配
- **触摸友好**: 按钮最小尺寸 44px
- **简化导航**: 汉堡菜单
- **垂直布局**: 单列布局
- **大字体**: 确保可读性

### 6.2 平板适配
- **双列布局**: 充分利用屏幕空间
- **触摸优化**: 保持触摸友好
- **侧边栏**: 可折叠侧边栏

### 6.3 桌面端适配
- **多列布局**: 充分利用宽屏
- **悬停效果**: 丰富的交互效果
- **快捷键**: 支持键盘操作

## 7. 可访问性设计

### 7.1 颜色对比度
- **文本对比度**: 至少 4.5:1
- **大文本对比度**: 至少 3:1
- **UI元素对比度**: 至少 3:1

### 7.2 键盘导航
- **Tab顺序**: 逻辑化的Tab顺序
- **焦点指示**: 清晰的焦点样式
- **快捷键**: 常用操作的快捷键

### 7.3 屏幕阅读器
- **语义化HTML**: 使用正确的HTML标签
- **ARIA标签**: 提供额外的可访问性信息
- **替代文本**: 为图片提供alt文本

## 8. 图标系统

### 8.1 图标风格
- **线性图标**: 简洁的线条风格
- **统一粗细**: 2px线条粗细
- **圆角处理**: 柔和的圆角
- **24px标准**: 标准尺寸24px

### 8.2 常用图标
- **导航图标**: 首页、机器人、数据、设置
- **操作图标**: 添加、编辑、删除、导出
- **状态图标**: 成功、警告、错误、加载
- **功能图标**: 搜索、筛选、排序、刷新

## 9. 设计资源

### 9.1 设计工具
- **Figma**: 主要设计工具
- **Sketch**: 备选设计工具
- **Adobe XD**: 原型设计

### 9.2 资源库
- **图标库**: Heroicons, Lucide Icons
- **图片资源**: Unsplash, Pexels
- **字体资源**: Google Fonts

### 9.3 设计系统
- **组件库**: 基于Tailwind CSS
- **设计令牌**: CSS变量管理
- **文档**: Storybook组件文档

## 10. 实施指南

### 10.1 开发规范
- **CSS类命名**: BEM方法论
- **组件化开发**: 可复用组件
- **响应式优先**: 移动端优先设计

### 10.2 质量保证
- **设计审查**: 定期设计审查
- **用户测试**: 用户反馈收集
- **性能优化**: 加载速度优化

### 10.3 维护更新
- **版本控制**: 设计系统版本管理
- **文档更新**: 及时更新设计文档
- **团队培训**: 设计规范培训 