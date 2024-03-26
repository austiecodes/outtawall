# outtawall

QauntumultX 可以通过使用资源解析器来使用 Surge 规则， Loon 原生支持。
Loon插件可以直接使用[这个](https://gitlab.com/lodepuly/vpn_tool/-/tree/master/Tool/Loon/Plugin?ref_type=heads)，本仓库的模组大部分也是改写自该仓库以适配 Surge 和 Stash。

## Surge 

解决被Google送中的问题：
```
https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt
```
这个规则集是 google 在中国大陆可以访问的域名集合。提前将这些域名加入代理可以防止被送中问题。

---

- 本仓库中部分的规则来自于 [Devine Engine](https://github.com/DivineEngine/Profiles)
- 使用了 [SukkaW](https://github.com/SukkaW/Surge) 的部分规则
- 使用了 [Loyalsoldier](https://github.com/Loyalsoldier/surge-rules) 的部分规则

---

给出 Surge 配置实例：
```
[Rule]
# A
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/AI/AI.list,AI,update-interval=172800
RULE-SET,https://ruleset.skk.moe/List/non_ip/apple_services.conf,Default
# Steam
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Game.list,DIRECT,update-interval=172800
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/SteamCommunity,Steam,update-interval=172800
# Streaming
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/YouTube.list,YouTube,update-interval=172800
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/DisneyPlus.list,DisneyPlus,update-interval=172800
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/PrimeVideo.list,PrimeVideo,update-interval=172800
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/Netflix.list,Netflix,update-interval=172800
RULE-SET,https://ruleset.skk.moe/List/non_ip/stream.conf,Netflix
RULE-SET,https://ruleset.skk.moe/List/ip/stream.conf,Netflix
# GoogleCN
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt,Default,update-interval=172800
# Telegram
RULE-SET,https://ruleset.skk.moe/List/non_ip/telegram.conf,Default,update-interval=172800
RULE-SET,https://ruleset.skk.moe/List/ip/telegram.conf,Default,update-interval=172800
RULE-SET,https://ruleset.skk.moe/List/ip/telegram_asn.conf,Default,update-interval=172800
# Reject Non IP
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject-drop.conf,DIRECT,update-interval=172800
DOMAIN-SET,https://ruleset.skk.moe/List/domainset/reject.conf,REJECT-TINYGIF
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject.conf,REJECT,update-interval=172800
# Reject IP
RULE-SET,https://ruleset.skk.moe/List/ip/reject.conf,DIRECT,update-interval=172800
# Misc
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Direct.list,DIRECT,update-interval=172800
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Global.list,Default,update-interval=172800
# Basic
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/direct.txt,DIRECT,update-interval=172800
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/prox
```

## Stash
- 提供基础的 yaml 模板 (可用于Clash for Windows 等)
- 根据个人使用和上游更新维护 Stash Overrides

