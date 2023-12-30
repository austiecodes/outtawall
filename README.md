# Mostly Based on Devine Engine

## Surge

* 解决被Google送中的问题:将 `https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt` 这个规则集改为代理. 这个规则集是 google 在中国大陆可以访问的域名集合,将这些域名加入代理可以解决被送中问题,但是因此YouTube会开启非常多的广告,所以需要配合 AdGuard 或者是 uBlock Origin 等插件来使用.

[Rule]

```

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Apple.list,DIRECT

RULE-SET,SYSTEM,DIRECT

RULE-SET,LAN,DIRECT

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/SteamCommunity.list,DIRECT

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/PrimeVideo.list,PrimeVideo

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Streaming/Netflix.list,Netflix

RULE-SET,https://github.com/austiecodes/outtawall/blob/main/Surge/PayPal.list,PayPal

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Direct.list,Direct

RULE-SET,https://raw.githubusercontent.com/austiecodes/outtawall/main/Surge/Global.list,Default

RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/telegramcidr.txt,Dafault

RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/ruleset/google.txt,Dafault

DOMAIN-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/reject.txt,REJECT

DOMAIN-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/private.txt,DIRECT

DOMAIN-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/direct.txt,DIRECT

RULE-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/cncidr.txt,DIRECT

DOMAIN-SET,https://cdn.jsdelivr.net/gh/Loyalsoldier/surge-rules@release/proxy.txt,Dafault

FINAL,Dafault
```

## Shadowrocket

复制该链接即可 `https://raw.githubusercontent.com/austiecodes/QXSR/main/ShadowRocket/abcd.conf`

