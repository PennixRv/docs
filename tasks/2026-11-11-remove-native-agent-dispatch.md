# 原生子代理路径移除文档收敛

本变更属于 Trellis `11-11-remove-native-agent-dispatch` 实施合同，覆盖当前英文、中文的配置、平台适配、Hook、角色、架构、命令和日常使用说明。当前角色统一为 `.trellis/agents/` 下的 Teamwork 与 Paseo 合同，普通 check Skill 和 Kiro 主入口保留；JSONL 改为按需创建的上下文数据。

最终候选推进至 beta.15，补齐 Reasonix 同路径替换及已知旧配置注释清理。beta.13、beta.14 的 CI 均在 npm 发布前主动取消，没有用于现场部署。两个旧候选的说明保留为候选历史，以 beta.15 及根任务实际验收为准。

历史 changelog 和示例保留历史属性，不作为当前可执行路由。新增 beta.13 双语发行说明，并按现有共享导航登记。`pnpm lint` 验证 707 个 Markdown/MDX 文件无错误，Beta/Release 共享导航一致。发布前由 Trellis 原生 changelog guard 核对精确候选。
