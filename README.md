# mihomo
自用Mihomo规则

```yaml
rule-providers:
  AI:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/ACL4SSR/refs/heads/master/Clash/Providers/Ruleset/AI.yaml"
    interval: 86400
    path: ./ACL4SSR/AI.yaml
  ChinaIp:
    behavior: ipcidr
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/ACL4SSR/refs/heads/master/Clash/Providers/ChinaIp.yaml"
    interval: 86400
    path: ./ACL4SSR/ChinaIp.yaml
  ChinaIpV6:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/ACL4SSR/refs/heads/master/Clash/Providers/ChinaIpV6.yaml"
    interval: 86400
    path: ./ACL4SSR/ChinaIpV6.yaml
  ChinaDomain:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/ACL4SSR/refs/heads/master/Clash/Providers/ChinaDomain.yaml"
    interval: 86400
    path: ./ACL4SSR/ChinaDomain.yaml
  LocalAreaNetwork:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/ACL4SSR/refs/heads/master/Clash/Providers/LocalAreaNetwork.yaml"
    interval: 86400
    path: ./ACL4SSR/LocalAreaNetwork.yaml
  DIRECT:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/mihomo/refs/heads/main/DIRECT.yaml"
    interval: 86400
    path: ./ACL4SSR/DIRECT.yaml
  PROXY:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/mihomo/refs/heads/main/PROXY.yaml"
    interval: 86400
    path: ./ACL4SSR/PROXY.yaml
  NodeSeek:
    behavior: classical
    type: http
    url: "https://github.180280.xyz/https://raw.githubusercontent.com/Yeqingky/mihomo/refs/heads/main/NodeSeek.yaml"
    interval: 86400
    path: ./ACL4SSR/NodeSeek.yaml

rules:
  - RULE-SET,DIRECT,DIRECT
  - RULE-SET,PROXY,代理
  - RULE-SET,NodeSeek,NodeSeek
  - RULE-SET,AI,AI
  - RULE-SET,ChinaIp,DIRECT
  - RULE-SET,ChinaIpV6,DIRECT
  - RULE-SET,ChinaDomain,DIRECT
  - RULE-SET,LocalAreaNetwork,DIRECT
  - MATCH,代理

```