# Next.js PPR (部分预渲染) 演示项目

这是一个展示 Next.js 15 部分预渲染 (Partial Prerendering) 功能的演示项目。PPR 允许页面同时包含静态预渲染内容和动态内容，提供最佳的用户体验和性能。

## 🚀 功能特性

- **静态预渲染**: 产品列表等静态内容在构建时预渲染，立即可见
- **动态加载**: 用户信息、分析数据等动态内容按需加载
- **渐进式加载**: 使用 Suspense 边界提供优雅的加载状态
- **响应式设计**: 支持深色模式和移动端适配
- **TypeScript**: 完整的类型安全支持

## 🛠️ 技术栈

- **Next.js 15.1.5-canary**: 支持 PPR 的 canary 版本
- **React 19**: 最新的 React 版本
- **TypeScript**: 类型安全
- **Tailwind CSS**: 样式框架
- **Geist 字体**: 现代化的字体

## 📁 项目结构

```
src/
├── app/
│   ├── layout.tsx          # 根布局
│   ├── page.tsx            # 首页
│   └── products/
│       └── page.tsx        # 产品页面
├── components/
│   ├── Analytics.tsx        # 分析数据组件
│   ├── Navigation.tsx      # 导航组件
│   ├── ProductList.tsx    # 产品列表组件
│   ├── SearchBar.tsx      # 搜索栏组件
│   ├── SearchResults.tsx  # 搜索结果组件
│   └── UserDashboard.tsx  # 用户仪表板组件
└── lib/
    └── data.ts            # 数据模拟和类型定义
```

## 🎯 PPR 演示场景

### 静态预渲染内容
- 产品列表: 构建时生成，立即可见
- 页面布局: 导航栏、标题等静态元素
- 搜索栏: 交互式但无需数据加载

### 动态加载内容
- 用户信息: 模拟从数据库获取用户数据
- 分析数据: 模拟实时分析数据
- 搜索结果: 根据查询动态生成

## 🚀 快速开始

1. **安装依赖**
   ```bash
   npm install
   # 或
   bun install
   ```

2. **启动开发服务器**
   ```bash
   npm run dev
   # 或
   bun dev
   ```

3. **访问应用**
   打开 [http://localhost:3000](http://localhost:3000) 查看演示

## 🔧 配置说明

### Next.js 配置
```typescript
// next.config.ts
const nextConfig: NextConfig = {
  experimental: {
    cacheComponents: true, // 启用组件缓存和 PPR
  },
};
```

### PPR 模式
- `true`: 启用组件缓存和部分预渲染
- `false`: 禁用组件缓存和 PPR

> **注意**: 在 Next.js 15.6+ 版本中，`experimental.ppr` 已被合并到 `experimental.cacheComponents` 中

## 📊 性能优势

1. **快速首屏**: 静态内容立即可见，无需等待
2. **渐进式加载**: 动态内容在后台加载，不阻塞页面渲染
3. **SEO 友好**: 静态内容对搜索引擎友好
4. **用户体验**: 优雅的加载状态和过渡效果

## 🎨 设计特色

- **现代化 UI**: 使用 Tailwind CSS 构建的现代化界面
- **深色模式**: 支持系统主题切换
- **响应式设计**: 适配各种屏幕尺寸
- **动画效果**: 流畅的加载动画和过渡效果

## 📝 学习要点

1. **Suspense 边界**: 使用 Suspense 包装动态组件
2. **数据获取**: 区分静态和动态数据获取
3. **加载状态**: 提供有意义的加载反馈
4. **错误处理**: 优雅地处理加载错误

## 🔗 相关资源

- [Next.js PPR 文档](https://nextjs.org/docs/app/building-your-application/rendering/partial-prerendering)
- [React Suspense](https://react.dev/reference/react/Suspense)
- [Next.js 15 新特性](https://nextjs.org/blog/next-15)

## 📄 许可证

MIT License
