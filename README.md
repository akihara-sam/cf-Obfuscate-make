
此代理源码来自 https://github.com/zaunist/cloudflare-proxy


自己添加了 自动混淆代码 功能



## 变量设置

**只需要设置 uuid 就行，如果不担心被其他人扫到，uuid 都不需要改，不过还是建议修改**

| 变量作用 | 变量名称 | 变量值要求 | 变量默认值 | 变量要求 |
|---------|----------|------------|------------|----------|
| 1、必要的uuid | uuid (小写字母) | 符合uuid规定格式 | 万人骑uuid：86c50e3a-5b87-49dd-bd20-03c7f2735e40 | 建议 |
| 2、订阅节点：优选IP | ip1到ip13，共13个 | CF官方IP、CF反代IP、CF优选域名 | CF官方不同地区的visa域名 | 可选 |
| 3、订阅节点：优选IP对应端口 | pt1到pt13，共13个 | CF13个标准端口、反代IP对应任意端口 | CF13个标准端口 | 可选 |
| 4、需要固定ip访问的网站 | proxydomains | 域名之间使用","分割 | "twitch.tv","ttvnw.net" | 可选 |
| 5、自定义重定向网站 | REDIRECT_URLS | 域名之间使用 回车 分割 | www.baidu.com 回车 www.qq.com 回车 www.cctv.com | 可选 |



在此基础上修改了代码  实现访问 域名后 可以重定向到 自定义的 网站，
只需在workers 中 添加 REDIRECT_URLS 变量 输入想要随机重定向的网站 按回车 添加多个站点。
