# Teamwork 文档路由与内容更新

## 目标

在 docs-site 当前 checkout 中，将稳定版和 Beta 版的中英文协作指南统一迁到 Teamwork 页面，并按 Trellis `v0.7.1` 当前 CLI、Skill 与已锁定设计重写内容。

## 范围

- 将 `advanced/channel.mdx`、`beta/advanced/channel.mdx`、`zh/advanced/channel.mdx` 和 `zh/beta/advanced/channel.mdx` 迁至对应的 `teamwork.mdx` 路由。
- 更新 `docs.json` 四个导航入口，删除旧活动页面且不建立重定向。
- 说明 one-shot、论坛、固定批次、teammate 通用角色与程序控制的批次完成边界；明确当前没有已验证宿主 adapter 时批次命令会在写入协调状态前拒绝。
- 历史 changelog 不在本任务范围内。

## 验收

- 稳定版与 Beta 版均有中英文 Teamwork 页面，内容与当前 CLI/Skill 合同一致；示例只使用实际存在的 `trellis teamwork` 命令。
- docs.json 可解析，四个导航路径均指向存在的页面；稳定版、Beta 版及对应语言页面之间链接正确。
- 活动文档无旧 `trellis channel` 命令、旧 Channel Skill 名称、旧活动路由或历史计费命令；历史 changelog 文件未改动。
- docs-site `pnpm lint` 与 `pnpm format:check` 通过。

## 明确排除

不修改 Trellis 产品源码、Skill、Marketplace、历史 changelog 或站点构建配置；不创建分支、不切换 checkout、不提交或推送。

## 2026-11-05 增量授权范围

当前根任务和 Trellis owner 的 `teamwork-input-result-remediation.md` 承接用户最新授权：同步 Beta 中英文 Teamwork 的输入分层、schema-2 内容报告、统一机器回执及自动允许权限语义，新增下一 beta 中英文发布说明与导航，并按既有发布逻辑提交推送当前分支。只增补新发布说明，不重写历史 changelog 或稳定版行为。该授权替代上文旧轮次的提交/推送排除；本仓没有原生任务运行时，不创建手写 task.json。
