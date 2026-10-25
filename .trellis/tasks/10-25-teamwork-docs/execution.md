# 实施记录

## 2026-10-25 文档路由迁移

- 状态：文档实现与针对性检查已完成；docs-site 没有原生 task 状态 CLI，本记录遵循其既有 PRD/execution 记录约定，不创建 `task.json`。
- checkout：`codex/chinese-user-templates`，基线 `aae956ee68dc6930bef802e0a1f74d91f18dc210`；开始时工作树干净。
- 依据：Trellis 当前 `trellis-teamwork` Skill、CLI 命令注册和 `trellis teamwork --help`。现有 Beta 文档中的 `teamwork sessions` 说明与当前注册命令树不符，迁移时应删除，不照搬。
- 已将稳定版、Beta 版的中英文指南迁至四个 `teamwork.mdx` 页面，并更新 `docs.json` 导航；旧活动页面已删除，无重定向。
- 页面按 Teamwork CLI/Skill 合同重写，涵盖 one-shot、固定批次与宿主 fail-closed 限制、独立评议、论坛和 Core Channel 命名边界。移除了旧的 `teamwork sessions` 历史计费段落，因为当前 CLI 没有该命令。
- `pnpm lint` 通过；本次四页、`docs.json` 和两份 owner 记录的 Prettier 定向检查通过。复核全站 `pnpm format:check` 后，当前结果为 118 个既有未格式化文件；与 docs-site 当前 10 个工作树变更路径无交集。未为此扩大改动范围。
- JSON 与四个导航路由校验通过；新页面互链有效，旧活动路由及 `trellis channel` / `trellis-channel` / 历史 `sessions --owner-session` 用法均不存在；历史 changelog 未改动。
- CLI help smoke 确认文档使用的 `teamwork run`、`create`、`post`、`forum`、`thread` 和 `batch` 命令及选项存在。未执行宿主运行时批次验收；当前宿主能力 gate 仍未通过，批次保持 fail-closed。
- docs-site 仍在 `codex/chinese-user-templates`，未创建或切换分支，未提交或推送。下一步转到既有 Marketplace `main` owner 步骤；根任务最终记录全站 formatter 的既有失败项。
- 后续用户明确要求提交相关内容并保持 Git 树干净；本次按该指示提交 docs-site 变更及父级 gitlink，不推送、不切换分支，也不接入正式工作流。
