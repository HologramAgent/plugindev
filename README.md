# plugindev

把 hmapdev 工具链封装成 Agent 可调用的工具：脚手架生成插件工程、构建打包 .hmap、管理 SDK 版本。配合 plugin_install 即可让 Agent 自己做完「新建插件 → 构建 → 安装」全流程。

HologramAgent 插件，随 SDK `1.0.0` 的示例插件拆分而来。

## 构建

```bash
hmapdev build
```

产物 `dist/plugindev_bundle.hmap` 经 `plugin_install` 安装。

## 自动更新

本仓库地址登记在 `plg.json` 的 `repo` 字段，安装后随产物写入
`plugin.json` 的 `repository` 字段 —— 内核的 `plugin_update` 靠它
从本仓库拉最新源码并重编安装。
