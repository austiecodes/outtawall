# outtwall
QauntumultX 可以通过使用资源解析器来使用 Surge 规则， Loon 原生支持。
Loon插件可以直接使用[这个](https://gitlab.com/lodepuly/vpn_tool/-/tree/master/Tool/Loon/Plugin?ref_type=heads)，本仓库的模组大部分也是改写该仓库以适配 Surge 和 Stash。

## Surge 

解决被Google送中的问题：将 `https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt` 这个规则集改为代理。这个规则集是 google 在中国大陆可以访问的域名集合,将这些域名加入代理可以解决被送中问题，但是因此 YouTube 会开启非常多的广告，所以需要配合 AdGuard 或者是 uBlock Origin 等插件来使用.

- 本仓库中部分的规则来自于 [Devine Engine](https://github.com/DivineEngine/Profiles)
- 使用了 [SukkaW](https://github.com/SukkaW/Surge) 的部分规则
- 使用了 [Loyalsoldier](https://github.com/Loyalsoldier/surge-rules) 的部分规则

给出 Surge 配置实例：
```
[Rule]
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt,Default
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/AI/AI.list,AI
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Apple.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/Netflix.list,Netflix
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/DisneyPlus.list,DisneyPlus
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/PrimeVideo.list,PrimeVideo
# Telegram
RULE-SET,https://ruleset.skk.moe/List/non_ip/telegram.conf,Default
RULE-SET,https://ruleset.skk.moe/List/ip/telegram.conf,Default
RULE-SET,https://ruleset.skk.moe/List/ip/telegram_asn.conf,Default
# Reject Non IP
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject-drop.conf,REJECT-DROP
DOMAIN-SET,https://ruleset.skk.moe/List/domainset/reject.conf,REJECT-TINYGIF
RULE-SET,https://ruleset.skk.moe/List/non_ip/reject.conf,REJECT
# Reject IP
RULE-SET,https://ruleset.skk.moe/List/ip/reject.conf,REJECT-DROP
# Misc
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Direct.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Global.list,Default
# Basic
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/direct.txt,DIRECT
RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/proxy.txt,Default
FINAL,Final
```

## Stash
- 提供基础的 yaml 模板(可用于Clash for Windows 等)
- 根据个人使用和上游更新维护 Stash Overrides

