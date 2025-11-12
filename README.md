# 简介

本项目生成适用于 [**Surge**](https://nssurge.com) 的规则集 RULE-SET

## 说明

本项目规则集（DOMAIN-SET 和 RULE-SET）的数据主要来源于项目 [@Loyalsoldier](https://github.com/Loyalsoldier/surge-rules) 

## 规则文件地址及使用方式

### 在线地址（URL）

> 如果无法访问域名 `raw.githubusercontent.com`，可以使用第二个地址（`cdn.jsdelivr.net`）



#### RULE-SET:

- **直连域名列表 direct.txt**：
  - [https://raw.githubusercontent.com/Ethan-T1/my-rules/refs/heads/main/direct.txt](https://raw.githubusercontent.com/Ethan-T1/my-rules/refs/heads/main/direct.txt)
  - [https://cdn.jsdelivr.net/gh/Ethan-T1/my-rules/main/direct.txt](https://cdn.jsdelivr.net/gh/Ethan-T1/my-rules@main/direct.txt)
- **代理域名列表 proxy.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/proxy.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/proxy.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/proxy.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/proxy.txt)
- **广告域名列表 reject.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/reject.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/reject.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/reject.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/reject.txt)
- **私有网络专用域名列表 private.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/private.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/private.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/private.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/private.txt)
- **Apple 在中国大陆可直连的域名列表 apple.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/apple.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/apple.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/apple.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/apple.txt)
- **iCloud 域名列表 icloud.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/icloud.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/icloud.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/icloud.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/icloud.txt)
- **[慎用] Google 在中国大陆可直连的域名列表 google.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/google.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/google.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt)
- **GFWList 域名列表 gfw.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/gfw.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/gfw.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/gfw.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/gfw.txt)
- **非中国大陆使用的顶级域名列表 tld-not-cn.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/tld-not-cn.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/tld-not-cn.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/tld-not-cn.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/tld-not-cn.txt)
- **Telegram 使用的 IP 地址列表 telegramcidr.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/telegramcidr.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/telegramcidr.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/telegramcidr.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/telegramcidr.txt)
- **中国大陆 IP 地址列表 cncidr.txt**：
  - [https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/cncidr.txt](https://raw.githubusercontent.com/Loyalsoldier/surge-rules/release/ruleset/cncidr.txt)
  - [https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/cncidr.txt](https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/cncidr.txt)

### 使用方式

关于 Surge 的详细使用方法，见[官方手册](https://manual.nssurge.com)。要想使用本项目的规则集，只需要在 Surge 配置文件中添加如下规则：

#### 白名单模式（推荐）

⚠️ 注意：

- 白名单模式，意为「**没有命中规则的网络流量，统统使用代理**」，适用于服务器线路网络质量稳定、快速，不缺服务器流量的用户。
- 以下配置中，除了 `DIRECT` 和 `REJECT` 是默认存在于 Surge 中的 policy（路由策略/流量处理策略），其余均为自定义 policy，对应配置文件中 `[Proxy]` 或 `[Proxy Group]` 中的代理名称。如你直接使用下面的 `[Rule]` 规则，则需要在 `[Proxy]` 或 `[Proxy Group]` 中手动配置一个名为 `PROXY` 的 policy。
- 如你希望 Apple、iCloud 和 Google 列表中的域名使用代理，则把 policy 由 `DIRECT` 改为 `PROXY`，以此类推，举一反三。

