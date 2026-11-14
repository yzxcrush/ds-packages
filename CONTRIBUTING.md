# 贡献包

- 包必须开源，根目录有 `ds.toml` 和 `src/<export>.ds`；
- tag 用语义化版本（`v0.1.0`）；
- 在 `index.json` 增加条目，`repo` 用 `user/repo`，`latest` 填最新 tag；
- 不接受需要执行安装脚本的包；
- 合并后可用 `dspm install <name>` 验证。
