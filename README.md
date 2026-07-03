# zhaoxisSkills

这个目录用于沉淀可复用的技能包，结构参考常见的技能仓组织方式。

## 目录约定

```text
zhaoxisSkills/
  skills/
    <group>/
      <skill-name>/
        SKILL.md
        references/
```

说明：

- `skills/`：技能主体目录
- `<group>/`：按领域或用途分组，例如 `dev`、`product`、`browser`
- `<skill-name>/`：单个技能目录，目录名与 frontmatter 里的 `name` 保持一致或高度接近
- `SKILL.md`：技能主文档
- `references/`：补充清单、模板、脚本、长文档参考资料

## 当前已收录

- `skills/dev/platform-microservice-integration-playbook`
  - 适用场景：基座壳平台中的后台应用、微前端应用、配套微服务接入与联调
  - 解决问题：组织隔离、导航树与列表不一致、跨域 iframe 上下文丢失、线上部署后数据异常、网关与配置链路错位

## 使用建议

1. 新项目开始接入前，先读对应技能的 `SKILL.md`
2. 联调和提测时，再配合 `references/` 里的检查清单逐项验证
3. 遇到新的高频坑，再把共性经验补回这个目录
