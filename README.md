# 门店经营系统 Skill

开源 Agent Skill：**门店经营系统建设**。

帮助 AI / 开发者在真实门店场景里设计与交付可用的经营系统流程——计费、预约、收银、库存、权限、状态流转、外部支付等。

仓库：[`mendian-jingying-xitong-skill`](https://github.com/Clarawang-duam/mendian-jingying-xitong-skill)

## 这个 Skill 做什么

- 写清**业务规则卡**（操作者、权限、前置条件、金额/状态、失败保留、重试、验收样例）
- 划清 UI / 服务端入口 / 业务写入边界
- 处理部分成功、幂等、并发与外部系统回调
- 按「给定数据 → 动作 → 可观察结果」做验收

## 快速使用

把本仓库当作 Agent Skill 安装（Cursor / Claude Code / WorkBuddy 等支持 `SKILL.md` 的工具均可）：

1. 阅读根目录 [`SKILL.md`](./SKILL.md)
2. 需要模板时查看 [`references/`](./references/)
3. 有参考编排时查看 [`agents/`](./agents/)

## 关键词

门店经营系统 · 门店经营系统 skill · 收银 · 预约核销 · 库存 · 计费 · 业务规则 · 验收测试 · Agent Skill

## License

MIT
