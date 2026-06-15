# contest2026_000_openvela

openvela AI 大赛 2026 参赛仓库（样例 / 模板，队伍编号 000）。

## 命名规范

`contest2026_<编号>_<队伍名>` — 编号三位零填充；队名 slug（全小写、英文/拼音、连字符）。
例：`contest2026_042_openvela`。

## 单队单仓 + 多形态子目录

每支队伍**只有一个仓库**，不同作品形态以**子目录**组织，由 manifest
（`contest2026_000_openvela.xml`）通过 `<linkfile>` 映射到 openvela 工程对应位置：

| 形态 | 仓库内子目录 | 映射到 openvela 路径 |
|---|---|---|
| 应用 | `app/hello_app/` | `packages/demos/contest2026_000_hello_app` |
| 快应用 | `quickapp/hello_quickapp/` | `packages/apps/contest2026_000_hello_quickapp` |
| 板级适配 | `board/contest_board/` | `vendor/openvela/boards/contest2026_000_board` |

## 拉取方式

```bash
repo init -u https://github.com/open-vela/contest2026_000_openvela \
  -b dev-ai-contest-2026 -m contest2026_000_openvela.xml
repo sync -j4 contest2026_000_openvela
```

同步后，整仓位于 `contest2026_000_openvela/`，各形态子目录通过软链接出现在上表
openvela 路径处。生产仓库零改动。

## 贡献

- 所有改动必须通过 **Pull Request** 合入（强制，无人可绕过）。
- 首次贡献需签署 CLA，PR 上会自动跑 `cla/signature` 检查；未签署按提示评论 `/check-cla` 复检。
