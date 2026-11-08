# 梁相官网

[`liang.today`](https://liang.today) 的 Astro 静态站，托管在 GitHub Pages。

## 本地开发

```bash
pnpm install
pnpm run dev
```

## 发布前检查

```bash
pnpm run test
pnpm run check
pnpm run build
```

插件开发使用个人 fork，PR 投向插件主仓 `main`，经 CI 与维护者审阅后集成，见[贡献指南](https://github.com/liang-today/dsh-liangxiang/blob/main/CONTRIBUTING.md)。官网改动同样使用个人 fork 的工作分支验证和发起审阅，正式发布经维护者批准后合入 `main`；推送 `main` 会触发 GitHub Actions 构建部署。正文页面位于 `src/pages/**/*.md`；视觉和交互集中在 Astro 布局、首页与 `src/styles/global.css`。

构建会优先同步社区后端快照。后端暂时不可用时，保留线上已发布的最后一份有效快照；线上快照也不可用时再使用仓库内的有效快照，不用假 `WAITING` 覆盖已知结果。

品牌与产品契约以插件仓库的 `AGENTS.md` 和 `docs/140-liangxiang-brand.md` 为准。当前官网不处理真实投票或 Token，只做产品介绍和本地交互演示。

安装入口统一指向 `/guide/`：Desktop 使用官方原生「插件 → 添加插件」，输入完整包名并安装、启用，提供三步图解；Cmd / Web 单独说明 profile 命令。公开版本信息跟随已发布版本，不随候选分支提前更新。

2.0.0工作分支准备在线钱包、梁股三盘与浅蓝水景说明，三张产品图为同一安装包的功能示例，依次主UI、梁股、梁祠；旧MP4保留历史链接，不再在首页自动播放。分享卡仍使用真实公开快照及其原有规则版本，不把示例数据写入今日快照。本分支尚未发布，官网线上仍以已部署版本为准。
