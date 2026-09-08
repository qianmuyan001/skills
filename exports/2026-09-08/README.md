# Skills 快照 — 2026-09-08

包含 509 个 SKILL.md：个人 99、系统内置 6、插件 404。

## 内容与来源

- `personal/skills/`：个人 Skills，汇集本机 Codex、Agents 和 Claude 的 Skills 目录；完全相同的文件夹仅存一份。
- `personal/variants/`：同名但内容不同的版本，保留来源目录，避免覆盖。
- `system/skills/`：Codex 内置 Skills 的备份，仅供参考。
- `plugins/`：本地缓存的插件 Skill 目录，保留厂商、插件名和版本；缓存存在不代表当前已启用。
- `manifest.json`：来源映射、去重记录、排除记录和各 Skill 的哈希。
- `SKILLS.md`：可浏览的 Skill 清单。
- `SHA256SUMS.txt`：包内文件校验值，校验文件自身除外。

插件只导出正式 `skills/` 目录和 ECC 的迁移命令 Skills，不重复收录其文档翻译、其他编辑器副本。原有许可证和声明随目录保留；本仓库根目录的许可证不替代第三方材料各自的许可。没有独立许可证的内容不因此获得额外授权。

未打包账号凭据、Codex 配置、记忆、对话历史、Git 历史、依赖安装目录、缓存、`.env*` 或密钥扫描基线。Skill 文档中原有示例、公开链接和路径保持原样。

## 恢复个人 Skills

在本目录执行 `python3 install_personal.py`。默认复制到 `~/.codex/skills/`，已存在的整个同名目录会跳过，不混合、不覆盖。可使用 `--destination /目标目录`。

安装完成后重新打开 Codex 或开始新会话，并检查 Skill 是否被发现。`microsoft-foundry` 等目录包含嵌套 Skills；不同工具的发现规则不同，可能需要按该工具说明单独配置。

同名变体需手动选择。系统和插件备份不会自动安装；插件依赖的 MCP、工具、运行时资源及账号连接应通过原插件安装流程恢复。此包不保证跨机器直接运行全部 Skills。

## 校验

macOS/Linux：`shasum -a 256 -c SHA256SUMS.txt`。
