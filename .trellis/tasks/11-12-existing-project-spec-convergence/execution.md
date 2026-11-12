# 文档执行与验证

同步当前线初始化、spec 结构和 bootstrap 的六份中英文说明，新增 `v0.7.2-beta.18` 双语 changelog 并接入现有 Beta/Release 共享 changelog 导航。registry 查询当前 beta.17，beta.18 tag 尚不存在。

所改八份 MDX 的 markdownlint 通过，Prettier 已核对，`pnpm lint:docs-json` 通过并确认共享组同步。原生发布前检查继续由 Trellis 执行，真实发布身份由根任务记录。本仓库没有可用原生任务运行时，沿已有 docs-only 记录方式维护，不手造任务状态。
