# Roadmap

[English](./roadmap.md) · [繁体中文](./roadmap.zh-TW.md)

本 repo 是一个持续维护中的个人 side project。下面的 roadmap 是规划,不是承诺 —— 项目会视实际使用回馈而调整。

## v1 — 已发布

- [x] **`superpowers-bridge`** — 串接 OpenSpec ↔ obra/superpowers,自带 `retrospective` artifact

## v1.x — 后续 backlog

这些项目记录在 `~/.claude/plans/pr-quizzical-oasis.md`(实作 plan):

- [ ] **`workflow-retrospective` skill 打包** — 目前 retrospective procedure 内嵌在 schema instruction 里(Decision 3)。如果有真实用户反映需要交互式调用 `/workflow-retrospective`(在 schema 流程之外),会把它升级成独立的 Claude Code plugin
- [ ] **End-to-end CI 集成测试** — 目前 CI 只跑 `openspec schema validate`。round-trip 测试(`/opsx:new` 一路到 `/opsx:archive`)能抓更多回归,但需要 Superpowers 进入 CI 环境
- [ ] **Verify artifact 5 处改进** — 列在 v1.1 backlog A(template 表达清晰、design 可选处理、worktree 来源、pass 标准、TDD 注记)

## 等 OpenSpec core

这几项在社群 schema 内无法解决,要等上游:

- [ ] **`requires_skills:` schema 字段** — 把 prompt 层的 PRECHECK 换成引擎验证的声明
- [ ] **`post_apply` phase** — 让 `verify` / `retrospective` 变成真正的 post-apply hook,而非带时序错位的 artifact(对应 spec-kit 的 `after_implement`)

## 未来 bridge 候选

实际需求出现时才加:

- [ ] **`obra-bridge`** — 广义对 obra/* 其他工具的集成(如果用户社群成长)
- [ ] **领域特定 schema** — 例如 `data-pipeline` 变体,加强 schema validation artifact

想提议新 bridge?到 <https://github.com/JiangWay/openspec-schemas/issues> 开 issue。
