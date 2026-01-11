# Auto-Synced DNS Blocklists for AdGuard Home

这是一个个人维护的 DNS 过滤规则同步仓库。利用 GitHub Actions 每天定时从上游源获取最新规则，并整合到一个仓库中，方便 AdGuard Home 调用。

**核心优势：**
1. **稳定备份**：即使上游源暂时无法访问，本地仓库仍有昨天的备份。
2. **国内加速**：配合 `gh-proxy` CDN，彻底解决 AdGuard Home 在国内更新规则失败或速度慢的问题。
3. **精选组合**：只收录适合国内网络环境的高质量规则。

## 📋 规则列表与加速链接 (CDN)

请直接将 **加速链接** 复制到 AdGuard Home 的 `过滤器` -> `DNS 封锁清单` 中。

| 规则名称 | 文件名 | 说明 |
| :--- | :--- | :--- |
| **Anti-AD** | `anti-ad.txt` | **主力推荐**。专为中文环境优化，命中率高，误杀率低。 |
| **Hagezi Pro** | `adblockplus.txt` | **全能选手**。包含隐私保护、去除电视/手机App广告，平衡性极佳。 |
| **AdRules (猫队)** | `adrules.txt` | **补充规则**。更新频繁，对国内视频网站和移动端广告覆盖较广。 |
| **Hagezi 防诈骗** | `adblockgambling.txt` | **安全防护**。专门拦截赌博、诈骗、恶意钓鱼网站，建议开启以保护家人。 |
| **AdGuard Base** | `adguarddnsfilter.txt` | **官方基础**。AdGuard 官方维护的基础过滤规则，作为兜底使用。 |

> ⚠️ **注意**：国内访问加速连接 https://gh-proxy.com/

```shell
# Anti-AD
https://hk.gh-proxy.org/https://github.com/vickai/AdGuardSDNSFilter/raw/refs/heads/main/rules/anti-ad.txt

# Hagezi Pro
https://hk.gh-proxy.org/https://github.com/vickai/AdGuardSDNSFilter/raw/refs/heads/main/rules/adblockplus.txt

# Hagezi 防诈骗
https://hk.gh-proxy.org/https://github.com/vickai/AdGuardSDNSFilter/raw/refs/heads/main/rules/adblockgambling.txt

# AdRules (猫队)
https://hk.gh-proxy.org/https://github.com/vickai/AdGuardSDNSFilter/raw/refs/heads/main/rules/adrules.txt

# AdGuard Base
https://hk.gh-proxy.org/https://github.com/vickai/AdGuardSDNSFilter/raw/refs/heads/main/rules/adguarddnsfilter.txt
```



## 🔄 更新机制
* **更新频率**：每天自动执行一次（北京时间上午 8:00）。
* **手动触发**：支持在 Actions 页面手动触发更新。

## 🛠️ 上游来源 (Credits)
感谢以下规则维护者的辛勤付出：

* **Anti-AD**: [https://anti-ad.net](https://anti-ad.net)
* **Hagezi (哈哥兹)**: [https://github.com/hagezi/dns-blocklists](https://github.com/hagezi/dns-blocklists)
* **AdRules (Cats-Team)**: [https://github.com/Cats-Team/AdRules](https://github.com/Cats-Team/AdRules)
* **AdGuard Team**: [https://github.com/AdguardTeam](https://github.com/AdguardTeam)

## ⚖️ 免责声明
本仓库仅作为规则的搬运工和同步工具，所有规则内容版权归原作者所有。
