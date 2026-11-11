# 原生子代理路径移除文档收敛

本变更属于 Trellis `11-11-remove-native-agent-dispatch` 实施合同，覆盖当前英文、中文的配置、平台适配、Hook、角色、架构、命令和日常使用说明。当前角色统一为 `.trellis/agents/` 下的 Teamwork 与 Paseo 合同，普通 check Skill 和 Kiro 主入口保留；JSONL 改为按需创建的上下文数据。

最终候选继续向前收敛。beta.13、beta.14 在 npm 发布前取消，beta.15 在干净检出门禁失败，均未部署。beta.16 修复旧 Gemini 角色测试后发布并完成首次原生更新；重复预览发现混合内容被错误登记为整文件模板基线的风险，尚未再次写入，用户内容完整。beta.17 修正指纹与后续覆盖边界，加入连续更新保护回归；最终部署与组合验收由根任务登记。

历史 changelog 和示例保留历史属性，不作为当前可执行路由。新增 beta.13 双语发行说明，并按现有共享导航登记。`pnpm lint` 验证 707 个 Markdown/MDX 文件无错误，Beta/Release 共享导航一致。发布前由 Trellis 原生 changelog guard 核对精确候选。
