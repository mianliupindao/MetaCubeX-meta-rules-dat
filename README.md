**下载地址**：

- **country.mmdb**
  - [Github release](https://github.com/MetaCubeX/meta-rules-dat/releases/download/latest/country.mmdb)
  - [JSdelivr](https://cdn.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/country.mmdb)
  - [JSdelivr-CF](https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/country.mmdb)
- **geoip.dat**

  - [Github release](https://github.com/MetaCubeX/meta-rules-dat/releases/download/latest/geoip.dat)
  - [JSdelivr](https://cdn.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geoip.dat)
  - [JSdelivr-CF](https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geoip.dat)

- **geoip.db**

  - [Github release](https://github.com/MetaCubeX/meta-rules-dat/releases/download/latest/geoip.db)
  - [JSdelivr](https://cdn.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geoip.db)
  - [JSdelivr-CF](https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geoip.db)

- **geosite.dat**

  - [Github release](https://github.com/MetaCubeX/meta-rules-dat/releases/download/latest/geosite.dat)
  - [JSdelivr](https://cdn.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geosite.dat)
  - [JSdelivr-CF](https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geosite.dat)

- **geosite.db**
  - [Github release](https://github.com/MetaCubeX/meta-rules-dat/releases/download/latest/geosite.db)
  - [JSdelivr](https://cdn.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geosite.db)
  - [JSdelivr-CF](https://testingcf.jsdelivr.net/gh/MetaCubeX/meta-rules-dat@release/geosite.db)

### country.mmdb,geoip.dat,geoip.db

同 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)
- 新增类别（方便有特殊需求的用户使用）：
  - `geoip:cloudflare`
  - `geoip:cloudfront`
  - `geoip:facebook`
  - `geoip:fastly`
  - `geoip:google`
  - `geoip:netflix`
  - `geoip:telegram`
  - `geoip:twitter`

### geosite.dat,geosite.db

用法同 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)  
  - `geosite:cn` 源替换为 [ChinaMax_Domain](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)
  - `geosite:steam@cn` 类别添加 [SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 的内数据
  - 新增类别
    - `geosite:biliintl` 来源 [biliintl](https://raw.githubusercontent.com/xishang0128/rules/main/biliintl.list)

## 示例
```yaml
  - GEOSITE,category-ads-all,REJECT
  - GEOSITE,private,DIRECT
  - GEOSITE,youtube,PROXY
  - GEOSITE,google,PROXY
  - GEOSITE,twitter,PROXY
  - GEOSITE,pixiv,PROXY
  - GEOSITE,category-scholar-!cn,PROXY
  - GEOSITE,biliintl,PROXY
  - GEOSITE,onedrive,DIRECT
  - GEOSITE,microsoft@cn,DIRECT
  - GEOSITE,apple-cn,DIRECT
  - GEOSITE,steam-cn,DIRECT
  - GEOSITE,category-games@cn,DIRECT
  - GEOSITE,geolocation-!cn,PROXY
  - GEOSITE,cn,DIRECT
  
  #GEOIP规则
  - GEOIP,private,DIRECT,no-resolve
  - GEOIP,telegram,PROXY
  - GEOIP,JP,PROXY
  - GEOIP,CN,DIRECT
  - DST-PORT,80/8080/443/8443,PROXY
  - MATCH,DIRECT
```
## 致谢

- [@Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)
- [@v2fly/domain-list-community](https://github.com/v2fly/domain-list-community)
- [@Loyalsoldier/domain-list-custom](https://github.com/Loyalsoldier/domain-list-custom)
- [@felixonmars/dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list)
- [@gfwlist/gfwlist](https://github.com/gfwlist/gfwlist)
- [@cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq)
- [@Loyalsoldier/cn-blocked-domain](https://github.com/Loyalsoldier/cn-blocked-domain)
- [@AdblockPlus/EasylistChina+Easylist.txt](https://easylist-downloads.adblockplus.org/easylistchina+easylist.txt)
- [@AdGuard/DNS-filter](https://kb.adguard.com/en/general/adguard-ad-filters#dns-filter)
- [@PeterLowe/adservers](https://pgl.yoyo.org/adservers)
- [@DanPollock/hosts](https://someonewhocares.org/hosts)
- [@crazy-max/WindowsSpyBlocker](https://github.com/crazy-max/WindowsSpyBlocker)
- [@blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
