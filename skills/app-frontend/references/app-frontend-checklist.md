# App 前端验证清单

- [ ] 当前运行模式已明确：App / H5 / 混合容器 / 浏览器
- [ ] 宿主上下文来源明确
- [ ] token 与组织切换逻辑明确
- [ ] locale / language 控制权来源明确
- [ ] H5 / App / PC 接口语义一致
- [ ] 页面回流后状态正确
- [ ] 真机与浏览器分别验证
- [ ] 多语言统一走 `@bluexii/shared-i18n`
- [ ] 移动端 token / 样式 / formatter 优先复用 `@bluexii/mobile-*`
- [ ] 宿主接管 `locale/language` 后，本地切换入口失效或隐藏
- [ ] 没有业务仓平行实现的 `DevLocaleSwitcher` / `LanguageSwitcher`
