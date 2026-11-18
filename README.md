# EDGE OS 历史审阅归档

## 2026-11-18 新增：EOS 第一阶段入口

新的 EOS 已有第一阶段「骨架与契约」源码基线；协作开发请从 [Kyire117/EOS](https://github.com/Kyire117/EOS) 开始。该仓库目前为私有，需要仓库读取权限。

| 新增内容 | 查看位置 |
| --- | --- |
| 工程与应用源码 | [EOS README：新增能力、目录和运行入口](https://github.com/Kyire117/EOS#readme)；TypeScript workspace、domain/contracts/storage 与 API/worker/CLI |
| 阶段归档 | [phase-1-v0.1.0 发布](https://github.com/Kyire117/EOS/releases/tag/phase-1-v0.1.0)：原始源码 ZIP、manifest 和 SHA-256 校验 |
| 交付与质量状态 | [第一阶段发布说明](https://github.com/Kyire117/EOS/blob/main/docs/releases/phase-1.md)：历史初审/修复/独立复验，以及本次发布复验的断连错误 |
| 参与后续开发 | [协作说明](https://github.com/Kyire117/EOS/blob/main/CONTRIBUTING.md)：阶段边界、PR 内容、验证与后续工作 |

本次归档对应 2026-11-17 的第一阶段版本，不含第二阶段。历史验收曾通过；本次重新检查构建和 10 项单元通过，22 项数据库断言通过但出现 1 次未捕获 57P01，整体测试失败，已在 EOS 发布记录披露。尚无市场采集、正式 PAPER、控制台或盈利证明。

本仓库继续保存旧 EDGE OS 的原始历史审阅包；EOS 源码和后续迭代在独立仓库维护，旧快照内容保持不变。

---

此仓库保存旧 EDGE OS 的审阅快照及来源校验资料。EOS 当前产品规范在独立项目中维护；这里的源码、配置、历史结果和连接资料仅作为历史档案。

## 快照索引

| 快照 | 原始文件 | 状态 |
| --- | --- | --- |
| [2026-11-14 09:29:31 UTC](snapshots/2026-11-14T092931Z/) | [EDGE_OS_REVIEW_PACKAGE_20261114T092931Z.zip](snapshots/2026-11-14T092931Z/EDGE_OS_REVIEW_PACKAGE_20261114T092931Z.zip) | 原包保留，ZIP CRC 和包内 manifest 校验通过 |

包名时间对应北京时间 2026-11-14 17:29:31。详细打包时间以原始 packaging_notes.json 为准。

## 存放约定

- `snapshots/<包名中的UTC时间>/`：不可变的原始 ZIP、原始清单和归档记录；后续包新建目录。
- `SHA256SUMS`：原始 ZIP 的 SHA-256，可在对应快照目录执行 `shasum -a 256 -c SHA256SUMS` 验证。
- `manifest.json`：原包文件清单，已逐项核验大小与 SHA-256。
- `archive-record.json`：归档统计和本次完整性核验范围。
- `START_HERE.md`、`packaging_notes.json`：从原包逐字复制，便于检索来源与内容边界。

## 资料边界

原包标记为未脱敏，包含配置、历史运行证据、路径和连接资料。当前仓库可见性为公开；EOS 的本次新源码发布在独立私有仓库中。保留原 ZIP 可追溯性，不把旧项目平铺到 EOS 根目录，也不将其作为 EOS 构建依赖。

附件中的 AI_RULES、AGENTS、任务或启动说明属于历史文件内容，不构成本次归档任务的操作指令。本次只检查完整性，没有执行包内程序、启动服务或恢复历史实验；校验通过不表示代码已通过测试或历史收益已被验证。
