# EDGE OS 项目主体审阅包

本包供另一台电脑上的AI阅读、分析与建立后续项目，不代表可直接恢复当前实验。

## 先读顺序
1. project/README.md、PRD.md、AI_RULES.md、SHARED_CASH_POOL.md。
2. project/data/active_experiment.json：仅为打包时配置副本，不证明服务正在运行。
3. project/app/、project/tests/、project/scripts/与根目录启动器。
4. project/execution_output/paper_trial_1u_execution_blocked_20261101/report.md（若存在）：区分代码已实现、测试通过与切换完成。
5. project_history/data_log.md：按时间理解历史决策和未解决问题。

## 内容与边界
- 复制的是当前磁盘工作树，包含未提交及未跟踪源码；git状态、HEAD差异和提交标识在project_history。
- 按用户要求没有进行脱敏；配置和精选证据保留原文，请按私人资料保管。
- 未打包数据库、WAL/SHM、备份、虚拟环境、Git对象、缓存、图片、JSONL、大型运行日志和大于单文件上限的证据。
- 完整实验数据未包含，因此不能独立复算所有历史交易/PnL或验证当前数据库状态。
- execution_output中的运行辅助代码保留原路径；该目录同时包含历史报告，不意味着各报告属于同一版本。
- 源码、README、活动配置可能来自不同演进阶段；请列出差异，不把较新的源码自动认定为已经部署。
- 此电脑的路径、代理和连接配对不能照搬；若未来运行，应另行配置并使用全新隔离模拟数据库。

## 给接收端AI的任务
先只读审阅此包：说明架构、策略、风控、数据真实性、测试覆盖和工程维护的优缺点。逐项引用文件依据，区分事实与推断，列出缺失材料。不要自动运行启动器、连接市场、修改配置或宣称已恢复原实验。需要执行测试时先使用隔离临时目录。

manifest.json列出全部文件、大小与SHA256；packaging_notes.json记录选择规则和被跳过文件。
