🎉船新项目：[ACL4SSR Mannix 订阅转换极速版](https://github.com/zsokami/cvt)

## ACL4SSR_Online_Full_Mannix.ini

自定义 订阅转换 配置转换 规则转换 的远程配置：

https://raw.githubusercontent.com/Fire-Dragons/ACL4SSR/main/ACL4SSR_Online_Full_Mannix.ini

修改自 
https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/config/ACL4SSR_Online_Full.ini
https://raw.githubusercontent.com/zsokami/ACL4SSR/main/ACL4SSR_Online_Full_Mannix.ini


## ACL4SSR_Online_Mannix.ini

去除国家/地区：

https://raw.githubusercontent.com/Fire-Dragons/ACL4SSR/main/ACL4SSR_Online_Mannix.ini


## ACL4SSR_Online_(Full_)Mannix_No_DNS_Leak.ini

无 DNS 泄漏：

https://raw.githubusercontent.com/Fire-Dragons/ACL4SSR/main/ACL4SSR_Online_Full_Mannix_No_DNS_Leak.ini

https://raw.githubusercontent.com/Fire-Dragons/ACL4SSR/main/ACL4SSR_Online_Mannix_No_DNS_Leak.ini

和原配置只有一行差异：

```diff
- ruleset=🛩️ ‍墙内,[]GEOIP,CN
+ ruleset=🛩️ ‍墙内,[]GEOIP,CN,no-resolve
```

原配置不在已知名单中的（国内外）域名会先通过当地 DNS 服务器解析一次。

添加 no-resolve 后，不在已知名单中的（国内外）域名将直接✈️ 起飞。

---

### 影视/动漫APP广告拦截

添加某些影视/动漫 APP 广告拦截规则：

https://raw.githubusercontent.com/zsokami/ACL4SSR/main/BanProgramAD1.list

附 hosts 文件（自动更新）：

https://raw.githubusercontent.com/zsokami/ACL4SSR/main/hosts

---


⚠ 重要！每个组名的**空格**后面都添加了一个**隐藏字符 \u200d** 用于防止与节点重名，改名需谨慎

移除
- 🇰🇷 韩国节点

重命名
- 🚀 节点选择 -> ✈️ 起飞
- 🚀 手动切换 -> 👆🏻 指定
- ♻️ 自动选择 -> ⚡ 低延迟
- 📺 哔哩哔哩 -> 📺 B站
- 🎯 全球直连 -> 🛩️ 墙内
- 🐟 漏网之鱼 -> 🌐 未知站点
- 🇭🇰 香港节点 -> 🇭🇰 香港
- 🇨🇳 台湾节点 -> 🇹🇼 台湾
- 🇸🇬 狮城节点 -> 🇸🇬 新加坡
- 🇯🇵 日本节点 -> 🇯🇵 日本
- 🇺🇲 美国节点 -> 🇺🇸 美国
- 🍎 苹果服务 -> 🍎 苹果
- 🎮 游戏平台 -> 🎮 游戏

合并
- 🛑 广告拦截 + 🍃 应用净化 -> 💩 广告
- Ⓜ️ 微软云盘 + Ⓜ️ 微软服务 + Ⓜ️ 微软Bing -> Ⓜ️ 微软
- 📹 油管视频 + 🎥 奈飞视频 + 🌍 国外媒体 + 📺 巴哈姆特 -> 🌍 外媒
- 🎶 网易音乐 + 📺 哔哩哔哩 + 🌏 国内媒体 -> 📺 ‍国媒
- 📲 电报消息 + 📢 谷歌FCM -> ✈️ 起飞

新增
- 🇨🇳 中国 (含 🇭🇰 香港 🇹🇼 台湾)
- 🎏 其他
- 🤖 ‍AI

url-test
- 延迟测试链接 http://www.gstatic.com/generate_204 -> https://i.ytimg.com/generate_204
- 间隔时间 300秒 -> 15/30秒
- 容差 50/150毫秒 -> 100/300毫秒

正则匹配大小写、简繁体，更好地匹配中转、IPLC节点

LocalAreaNetwork.list 使用 DIRECT

移除 Download.list
