# outtwall

## Surge
- 解决被Google送中的问题：将 `https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt` 这个规则集改为代理。这个规则集是 google 在中国大陆可以访问的域名集合,将这些域名加入代理可以解决被送中问题，但是因此YouTube会开启非常多的广告，所以需要配合 AdGuard 或者是 uBlock Origin 等插件来使用.

- 本仓库中部分的规则来自于 Devine Engine
- 使用了 SukkaW 的 ip and non-ip reject
- 使用了 Loyalsoldier 的 DIRECT 和 Proxy 列表


```
[Rule]
# AI and Apple
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/AI/AI.list,Default
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Apple.list,DIRECT
# Streaming
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/Netflix.list,Netflix
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/DisneyPlus.list,DisneyPlus
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/PrimeVideo.list,PrimeVideo
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/Spotify.list,Default
# Basic Part
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Direct.list,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt,Default
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Global.list,Default
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/cncidr.txt,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/direct.txt,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/telegramcidr.txt,Default
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/proxy.txt,Default
# Non IP Reject
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject-drop.conf,REJECT-DROP
DOMAIN-SET,https://ruleset.skk.moe/List/domainset/reject.conf,REJECT-TINYGIF
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject.conf,REJECT
# IP Reject
RULE-SET,https://ruleset.skk.moe/List/ip/reject.conf,REJECT-DROP
FINAL,Final
```

## Stash
- 提供基础的 yaml 模板
- 根据个人使用和上游维护 Stash Overrides

