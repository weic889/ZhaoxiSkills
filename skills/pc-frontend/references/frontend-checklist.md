# PC 前端验证清单

- [ ] 当前页面模式已分类清楚
- [ ] `PcListPageLayout` / `PcToolbar` / `PcTableBottomBar` / `FormEntrySpec` 复用策略明确
- [ ] 菜单 key、路由、资源 code 一致
- [ ] 树、筛选、列表字段模型一致
- [ ] 请求头组织字段正确
- [ ] 切组织后重新拉树和列表
- [ ] 新增、编辑、详情一起验证
- [ ] 菜单选中态不丢失
- [ ] 分页真实驱动请求
- [ ] 多语言统一走 `@bluexii/shared-i18n`
- [ ] `DEV` 本地语言切换通过公共入口验证
- [ ] `QA / UAT / Prod` 下本地语言切换入口不可见
- [ ] 宿主传入 `locale/language` 后，本地切换入口失效或隐藏
- [ ] 跨域 `iframe` / 模块式 React 子应用已验证宿主 URL、标签缓存、内部路由一致
- [ ] `dist/index.html` 不残留 `/assets/...`
