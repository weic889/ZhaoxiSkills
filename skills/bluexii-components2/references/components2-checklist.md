# Bluexii Components2 接入清单

## 开工前

- [ ] 先读 `bluexii-components2/README.md`
- [ ] 确认当前任务属于 PC 公共层、移动公共层还是跨端基础设施
- [ ] 确认当前页面模式：列表页、详情页、表单页、双栏页、统计页、弹窗/抽屉页
- [ ] 确认当前页面必须直接复用哪些公共能力
- [ ] 确认这次改动属于公共仓还是业务仓

## 公共能力映射

- [ ] 跨端多语言：`@bluexii/shared-i18n`
- [ ] 跨端 token：`@bluexii/shared-tokens`
- [ ] 跨端工具：`@bluexii/shared-utils`
- [ ] PC 壳层：`@bluexii/pc-shell`
- [ ] PC UI：`@bluexii/pc-ui`
- [ ] PC 表单 schema / renderer：`@bluexii/pc-form-engine`
- [ ] PC 表单设计器：`@bluexii/pc-form-designer`
- [ ] 移动端 UI / token / styles / formatter：`@bluexii/mobile-*`

## 开发中

- [ ] 不在业务仓平行重写公共壳层、公共筛选区、公共分页、公共表单规范
- [ ] 不使用伪元素或 `row-reverse` 手工画必填标识
- [ ] 公共依赖版本保持一致，不只升级单个包
- [ ] 需要老应用迁移时，再读公共仓里的 `bluexii-legacy-app-refactor`
- [ ] 需要 PC 发版治理时，再读公共仓里的 `bluexii-pc-governance-check`

## 提测前

- [ ] token、baseURL、环境配置正确
- [ ] 分页真实生效
- [ ] 多语言切换覆盖当前页
- [ ] 公共背景、边距、按钮区、滚动边界已吃到公共样式
- [ ] 权限按钮显隐正确
- [ ] 没有残留硬编码中文

## 壳层和宿主联动

- [ ] 宿主传入 `locale/language` 后，业务仓能回到宿主管控
- [ ] 跨域 `iframe` 或模块式 React 子应用已验证宿主路由同步
- [ ] 刷新后能回到真实内部页，不是只回首页
- [ ] 标签缓存、外层 URL、内部路由状态一致
- [ ] `QA / UAT / Prod` 下本地调试语言切换入口完全不可见
