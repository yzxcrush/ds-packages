# ds-packages — dspm 包索引

这是 [dspm](https://github.com/yzxcrush/ds/blob/main/docs/DSPM.md) 的默认包索引：
短名 → GitHub repo。**无中心服务器**，索引就是一个 GitHub 文件。

安装示例：

```bash
./dspm search hello
./dspm install ds-hello
```

索引 URL（dspm 默认）：
`https://raw.githubusercontent.com/yzxcrush/ds-packages/main/index.json`

## 提交你的包

1. 在 GitHub 建仓库，根目录 `ds.toml` + `src/<export>.ds`，打 tag（如 `v0.1.0`）；
2. Fork 本仓库，在 `index.json` 的 `packages` 加：

```json
"your-name": {
  "repo": "your-user/your-repo",
  "summary": "一句话说明",
  "latest": "v0.1.0",
  "tags": ["v0.1.0"],
  "targets": ["app", "bare"],
  "exports": ["your_module"]
}
```

3. 提 PR；合并后用户即可 `dspm install your-name`。

## 安全

- dspm 只解压源码，不执行任何 build/install 脚本；
- `@asm/@raw` 等包会被扫描为 `unsafe` 并要求确认；
- index 仅做短名映射，不托管代码。
