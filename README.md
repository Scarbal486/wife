## Aastrbot抽二次元老婆插件图床仓库

**如果需要快速响应，请下载全部图片放入AstrBot\data\plugin_data\astrbot_plugin_animewifex\img\wife目录。**

## Deno Deploy部署
**相比Cloudflare Workers，优点是免代理访问。**

**首先Fork本仓库**

首页：https://deno.com/deploy 

先注册登陆，点击`New Playground`
![D1](/D1.png)
复制粘贴 [Deno Deploy.ts](https://raw.githubusercontent.com/monbed/wife/refs/heads/main/Deno%20Deploy.ts) 中的代码，然后点击`Save Deploy`。
![D2](/D2.png)
返回面板点击`Settings`。
![D3](/D3.png)
在`Environment Variables`中添加

根据你的实际情况修改下列配置

GITHUB_OWNER=monbed

GITHUB_REPO=wife

GITHUB_BRANCH=main

GITHUB_TOKEN=你的GITHUB_TOKEN

GITHUB_TOKEN在这申请https://github.com/settings/tokens
![D4](/D4.png)
点击`Save`。

在插件填入URL时，在结尾加上"/"，如https://clever-toad-16.deno.dev/

## Cloudflare Workers部署
**首先Fork本仓库**

首页：https://workers.cloudflare.com

先注册登陆，选择左侧`Compute (Workers)`，然后点击`Workers Pages`，`Start with Hello World!`。![1](/1.png)
取一个子域名（自己喜欢），点击`Deploy`。![2](/2.png)
完成后点击Edit code，复制 [Cloudflare Workers.js](https://raw.githubusercontent.com/monbed/wife/refs/heads/main/Cloudflare%20Workers.js)  到左侧代码框
![3](/3.png)

如果点错了可以在此处找到代码修改处：![4](/4.png)


根据你的实际情况修改下列配置

const OWNER        = 'monbed'

const REPO         = 'wife'

const BRANCH       = 'main'

// 访问私有仓库需 repo Scope，公共仓库建议 public_repo

const GITHUB_TOKEN = '' 


GITHUB_TOKEN在这申请https://github.com/settings/tokens

最后点击`Deploy`。如果正常，右侧应显示首页。

在插件填入URL时，在结尾加上"/"，如https://113123.258369.workers.dev/


由于Cloudflare Workers被墙，请给bot可以正确访问的网络，或者其它可访问的方式（Google）。

## 致谢
本仓库大部分图片出自（本人也添加了些）：   

https://github.com/Rinco304/AnimeWife

https://github.com/zgojin/astrbot_plugin_AW

https://t.me/WaifuP1c
