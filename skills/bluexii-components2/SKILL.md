---
name: bluexii-components2
description: 用于接入、复用或校验 Bluexii 前端公共仓 bluexii-components2，尤其适合处理 PC 壳层、公共 UI、表单引擎、多语言、主题 token、移动端公共组件以及提测发版前需要先确认公共边界和统一接入顺序的场景。
---

# Bluexii Components2

## 概述

这个技能用于处理 `bluexii-components2` 公共仓接入、复用和治理问题。

核心原则：

1. 公共的修公共，业务的修业务。
2. 先读公共仓唯一入口，再决定要读哪个专项文档。
3. 壳层、页面骨架、token、多语言、通用组件优先复用公共仓，不在业务仓平行重写。

## 何时使用

- 业务仓开始接入 `@bluexii/*` 公共包
- PC、App、H5、门户前端需要确认该复用哪些公共能力
- 页面样式、壳层、分页、筛选区、表单规范开始出现业务仓自写变体
- 提测或发版前需要确认是否真正按公共仓规范接入

## 核心模式

### 唯一入口

- 默认先读 `bluexii-components2/README.md`
- 不要先翻多个 README 再自己猜目录
- 只有命中专项时，再读补充文档或专项 skill

### 公共包分层

- `shared-i18n`、`shared-tokens`、`shared-utils` 负责跨端基础设施
- `pc-shell`、`pc-ui`、`pc-form-engine`、`pc-form-designer` 负责 PC 公共层
- `mobile-ui`、`mobile-tokens`、`mobile-styles`、`mobile-formatters` 负责移动端公共层
- 业务仓不承载公共壳层、公共页面骨架、公共 token 的平行实现

### 固定接入顺序

1. 先确认仓库定位和接入总口径
2. 再确认当前页面属于哪种标准模式
3. 再确认当前页面必须复用哪些公共能力
4. 最后才写业务仓定制代码

### 公共边界

- 壳层、布局骨架、筛选区、表格底部分页、表单录入规范默认属于公共层
- 业务字段、业务校验、业务流程编排默认留在业务仓
- 如果一个问题会在多个业务仓重复出现，优先判断是否应该回推公共仓

## 常见错误

- 还没读公共仓入口就直接在业务仓写页面
- 公共仓已有 `PcListPageLayout`、`PcToolbar`、token、多语言切换方案，业务仓仍自写近似版本
- 只升级一个公共包，忽略依赖链里其他 `@bluexii/*` 包的版本一致性
- 提测前只看页面显示，不验证 token、分页、宿主路由同步和本地多语言调试入口

## 参考资料

- [Bluexii Components2 接入清单](./references/components2-checklist.md)
