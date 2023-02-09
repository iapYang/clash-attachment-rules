# clash-attachment-rules
自用clash补充规则，主要规则引用自[clash-rules](https://github.com/Loyalsoldier/clash-rules)，本文为自用补充规则

### 使用方式
要想使用本项目的规则集，只需要在 Clash 配置文件中添加如下 rule-providers 和 rules。

#### Rule Providers 配置方式
```yaml
rule-providers:
  iapyang-proxy:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/iapYang/clash-attachment-rules/main/rules/proxy.txt"
    path: ./ruleset/iapyang-proxy.yaml
    interval: 86400

  iapyang-direct:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/iapYang/clash-attachment-rules/main/rules/direct.txt"
    path: ./ruleset/iapyang-direct.yaml
    interval: 86400
```

#### Rules配置方式
```yaml
rules:
  - RULE-SET,iapyang-proxy,PROXY
  - RULE-SET,iapyang-direct,DIRECT
```