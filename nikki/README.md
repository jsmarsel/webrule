# Nikki / Mihomo 配置模板

[`separated-providers.yaml`](./separated-providers.yaml) 是一份可复用的 Nikki 配置模板，包含：

- 一个外部代理 Provider，节点统一归入 `PROXY` 手工选择组
- `AUTO` 自动测速与 `FALLBACK` 故障转移
- AI、YouTube、Netflix、Google、Telegram、Twitter、GitHub、Spotify、Microsoft、Apple 分组
- MetaCubeX `mrs` 外部规则，规则每 24 小时更新一次
- 国内、局域网直连，广告拒绝，其余流量走 `PROXY`

## 使用方法

1. 下载 [`separated-providers.yaml`](./separated-providers.yaml)。
2. 把文件中的 `REPLACE_WITH_YOUR_PROVIDER_SUBSCRIPTION_URL` 替换为自己的代理订阅地址。
3. 在 Nikki 的“配置文件”页面上传该文件并设为当前配置，然后启动或重启 Nikki。
4. 打开面板，确认 `provider-1` 已更新且 `PROXY` 中能看到订阅节点。

合并到 `main` 后，也可以从下面的固定地址下载模板：

```text
https://raw.githubusercontent.com/jsmarsel/webrule/main/nikki/separated-providers.yaml
```

这份文件只保存代理 Provider、策略组和分流规则。TUN、DNS、控制端口等运行参数继续由 Nikki 的混入配置管理。

## 安全说明

本仓库是公开仓库。不要提交真实订阅地址、订阅令牌、Nikki 面板密钥、路由器密码或其他凭据。每次提交前都应确认模板仍使用占位符。
