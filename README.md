# TikTok 数据接口（TikTok API）：视频搜索、评论、达人、话题、字幕、广告库、TikTok Shop

**TikTok API · TikTok video search · TikTok comments · TikTok transcripts · TikTok ads · TikTok Shop products**

这个仓库是 [DataXAPI](https://dataxapi.com/zh/?ref=gh-tiktok-api) 的TikTok接口说明和能直接跑的脚本：19 个接口，一把 Key，按次付费，$0.002 起，**出错不收费**。不用登录平台账号，不用 Cookie，不开浏览器。

[免费拿 Key：试用最多 333 次，不用绑卡](https://dataxapi.com/zh/signin/?button=gh-tiktok-api) · [全部接口文档](https://dataxapi.com/zh/apis/?ref=gh-tiktok-api) · [接进 AI（MCP）](#接进-aimcp) · [English](#english)

最低充 $10，余额不过期；支持支付宝、微信支付和银行卡。

## 全部 19 个接口

### 广告

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 广告库搜索](https://dataxapi.com/zh/apis/tiktok/ads/search/?ref=gh-tiktok-api) | 按关键词或广告主名字搜 TikTok 公开广告库（欧洲地区投放的广告）：广告主、标题、视频和图片素材、首次和最近一次展示的时间、触达人数档位；最新的在前，一页 12 条。这是广告透明度记录，和创意中心的热门广告是两份数据。 | $0.002 一次 | `tiktok.ads.search` |
| [TikTok 广告库广告详情](https://dataxapi.com/zh/apis/tiktok/ads/get/?ref=gh-tiktok-api) | 按编号或链接取 TikTok 公开广告库里的一条广告：广告主、标题、视频和图片素材、落地页、首次和最近一次展示的时间、投放的国家、投放目标。 | $0.002 一次 | `tiktok.ads.get` |

### 评论

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 评论回复](https://dataxapi.com/zh/apis/tiktok/comments/replies/list/?ref=gh-tiktok-api) | 按评论编号和它所在的视频编号取一页回复，每页 20 条：正文、回复者、点赞数、发布时间、回复的是哪一条。 | $0.002 一次 | `tiktok.comments.replies.list` |

### 创意中心

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 创意中心热门广告详情](https://dataxapi.com/zh/apis/tiktok/creative_center/ads/get/?ref=gh-tiktok-api) | 按编号取 TikTok 创意中心的一条热门广告（Top Ads）：广告视频、文案、品牌名、落地页、点赞数、评论数、分享数、时长、投放目标、行业代号、投放的国家。 | $0.002 一次 | `tiktok.creative_center.ads.get` |
| [TikTok 创意中心热门广告搜索](https://dataxapi.com/zh/apis/tiktok/creative_center/ads/search/?ref=gh-tiktok-api) | 按关键词搜 TikTok 创意中心的热门广告（Top Ads）：广告视频、文案、品牌名、点赞数、时长、投放目标；一次看一个国家，可选统计周期，按推荐或点赞数排序。一页 20 条。这是表现好的广告素材展示，不是广告库：没有投放时间。 | $0.002 一次 | `tiktok.creative_center.ads.search` |

### 话题标签

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 话题作品](https://dataxapi.com/zh/apis/tiktok/hashtags/videos/list/?ref=gh-tiktok-api) | 按话题名取一页带这个话题的 TikTok 视频，每页约 20 条：文案、作者、互动数、封面和播放地址。 | $0.002 一次 | `tiktok.hashtags.videos.list` |

### 账号

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 用户资料](https://dataxapi.com/zh/apis/tiktok/users/get/?ref=gh-tiktok-api) | 按账号名或编号取 TikTok 用户资料：显示名、简介、粉丝数、关注数、作品数、获赞数、是否认证。 | $0.002 一次 | `tiktok.users.get` |
| [TikTok 用户搜索](https://dataxapi.com/zh/apis/tiktok/users/search/?ref=gh-tiktok-api) | 按关键词搜索 TikTok 账号，每页 30 个：账号名、显示名、粉丝数、关注数、作品数、获赞数。 | $0.002 一次 | `tiktok.users.search` |
| [TikTok 用户作品](https://dataxapi.com/zh/apis/tiktok/users/videos/list/?ref=gh-tiktok-api) | 按账号名取一页 TikTok 用户发布的视频，每页 10 条：文案、互动数、发布时间、封面和播放地址，可按最新或最热排。 | $0.002 一次 | `tiktok.users.videos.list` |
| [TikTok 用户粉丝列表](https://dataxapi.com/zh/apis/tiktok/users/followers/list/?ref=gh-tiktok-api) | 按账号名取一页关注该 TikTok 用户的账号，每页 50 个，从最新关注的开始：账号名、显示名、简介、粉丝数、关注数、作品数、获赞数，以及账号的国家或地区和语言，可看粉丝分布。 | $0.002 一次 | `tiktok.users.followers.list` |

### 视频

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok 视频评论](https://dataxapi.com/zh/apis/tiktok/videos/comments/list/?ref=gh-tiktok-api) | 按视频编号或链接取一页 TikTok 评论，每页 50 条：正文、评论者和评论者账号的国家或地区、点赞数、回复数、发布时间。 | $0.002 一次 | `tiktok.videos.comments.list` |
| [TikTok 视频详情](https://dataxapi.com/zh/apis/tiktok/videos/get/?ref=gh-tiktok-api) | 按视频编号或链接取一条 TikTok 视频：文案、作者、点赞评论分享收藏播放数、封面和播放地址。 | $0.002 一次 | `tiktok.videos.get` |
| [TikTok 视频搜索](https://dataxapi.com/zh/apis/tiktok/videos/search/?ref=gh-tiktok-api) | 按关键词搜索 TikTok 视频，每页 30 条，可按相关度、点赞数或发布时间排，可限定发布时间。 | $0.002 一次 | `tiktok.videos.search` |
| [TikTok 视频字幕](https://dataxapi.com/zh/apis/tiktok/videos/transcript/get/?ref=gh-tiktok-api) | 按视频编号或链接取 TikTok 视频里说的话：全文和带时间的分段，可用 lang 指定字幕语言。 | $0.002 一次 | `tiktok.videos.transcript.get` |
| [TikTok 无水印视频下载地址](https://dataxapi.com/zh/apis/tiktok/videos/media/get/?ref=gh-tiktok-api) | 给一条 TikTok 视频或图文的编号或链接，返回它的全部文件地址：无水印视频的各档清晰度（带宽高、编码、码率、大小和过期时间）、封面、背景音乐，图文另给每张图片。签名里写了过期时间的都给出 expires_at，过期了再调一次即可。 | $0.002 一次 | `tiktok.videos.media.get` |

### 商城商品

| 接口 | 拿到什么 | 价格 | 编号 |
|---|---|---|---|
| [TikTok Shop 商品详情](https://dataxapi.com/zh/apis/tiktok/shop/products/get/?ref=gh-tiktok-api) | 按商品编号取 TikTok Shop 美国站的一件商品：标题、文字说明、图片、评分、评价数、已售件数，店铺和它的评分、粉丝数、在售商品数，商品页上显示的价格和运费。页面价比店铺列表和搜索里的价格高约一个运费，列表价用商品搜索取。 | $0.002 一次 | `tiktok.shop.products.get` |
| [TikTok Shop 商品评价](https://dataxapi.com/zh/apis/tiktok/shop/products/reviews/list/?ref=gh-tiktok-api) | 按商品编号取 TikTok Shop 美国站这件商品排在最前的 10 条买家评价：正文、评分、时间、买的规格、晒图。 | $0.002 一次 | `tiktok.shop.products.reviews.list` |
| [TikTok Shop 商品搜索](https://dataxapi.com/zh/apis/tiktok/shop/products/search/?ref=gh-tiktok-api) | 按搜索词取 TikTok Shop 美国站的商品：标题、现价和原价、评分、已售件数、店铺。 | $0.002 一次 | `tiktok.shop.products.search` |
| [TikTok Shop 店铺商品](https://dataxapi.com/zh/apis/tiktok/shop/sellers/products/list/?ref=gh-tiktok-api) | 按店铺编号取一页这家 TikTok Shop 美国站店铺在售的商品：标题、现价和原价、评分、评价数、已售件数。 | $0.002 一次 | `tiktok.shop.sellers.products.list` |

## 真实返回长什么样

**TikTok 视频搜索**（`tiktok.videos.search`，参数 `{"query":"space station"}`），录下的真实返回，个人信息换成了 …：

```json
{
  "data": {
    "items": [
      {
        "id": "…",
        "url": "https://example.com/…",
        "type": "video",
        "text": "…",
        "lang": "en",
        "published_at": "2026-10-11T23:17:34.000Z",
        "author": {
          "id": "…",
          "username": "…",
          "name": "…",
          "avatar_url": "https://example.com/…",
          "followers": 92601
        },
        "metrics": {
          "likes": 353,
          "comments": 11,
          "shares": 19,
          "favorites": 40,
          "views": 7561
        },
        "hashtags": [
          "…",
          "…"
        ],
        "mentions": []
      }
    ]
  },
  "page": {
    "next_cursor": "example-cursor-1",
    "cursor_expires_at": "2026-10-12T20:17:24.000Z",
    "has_more": true,
    "returned": 30
  }
}
```

每个接口都是同一种结构：列表在 `data.items`，单个在 `data.item`，下一页用 `page.next_cursor`，这次扣了多少在 `meta.billing.amount`，平台不给的字段为 `null` 并在 `meta.unavailable` 里写明。

## 快速开始

1. [拿一把 Key](https://dataxapi.com/zh/signin/?button=gh-tiktok-api)（`dx_` 开头），放进环境变量：`export DATAXAPI_API_KEY=dx_...`
2. 调一次接口：

```bash
curl -G "https://api.dataxapi.com/v1/tiktok/videos/search" \
  -H "Authorization: Bearer $DATAXAPI_API_KEY" \
  --data-urlencode 'query=space station'
```

3. 或者跑 `examples/` 里的脚本。只用 Python 标准库（3.9 以上）；不加 `--yes` 只报价、不调用，加了才真跑，跑完告诉你实际花了多少：

| 脚本 | 做什么 | 先看要花多少 |
|---|---|---|
| [quickstart.py](examples/quickstart.py) | 取几页结果，存成 CSV | `cd examples && python3 quickstart.py 'space station'` |

## 接进 AI（MCP）

Claude Code：

```bash
claude mcp add --transport http --scope user dataxapi https://api.dataxapi.com/mcp --header "Authorization: Bearer $DATAXAPI_API_KEY"
```

Cursor、Cherry Studio、WorkBuddy 等支持远程 MCP 的客户端：

```json
{
  "mcpServers": {
    "dataxapi": {
      "url": "https://api.dataxapi.com/mcp",
      "headers": {
        "Authorization": "Bearer dx_..."
      }
    }
  }
}
```

接上以后直接用中文问，比如“帮我看看这个关键词最近一个月在抖音上的热度”。AI 花钱前可以先免费查接口和价格。也可以装成技能：`npx skills add data-x-api/skills`。

## 常见问题

**要不要平台账号、Cookie 或扫码？**

不要。只要一把 DataXAPI Key，不碰你的账号，也就不存在账号被风控的问题。

**调用出错扣钱吗？**

不扣。每次返回里的 `meta.billing.amount` 写明这次扣了多少（美元）。

**数据有多新？**

默认在你调用时从平台实时读取，返回里的 `meta.fetched_at` 写明读取时间。

**怎么翻页？**

列表接口一次返回一页，把返回里的 `page.next_cursor` 作为 `cursor` 传回去取下一页，每一页单独计费。

## English

TikTok API: video search, comments, creators, hashtags, transcripts, the ad library, Creative Center and TikTok Shop, through one key, paid per call.

No platform account, cookie or QR login. Paid per call from $0.002; errors are not charged. Free trial: up to 333 calls, no card. [Get a key](https://dataxapi.com/signin/?button=gh-tiktok-api) · [All endpoints](https://dataxapi.com/apis/?ref=gh-tiktok-api) · MCP: `https://api.dataxapi.com/mcp`.

## License

MIT

<sub>接口和价格取自 DataXAPI 的目录 0051cce45e9530b9、价格版本 22；以 [dataxapi.com/zh/apis](https://dataxapi.com/zh/apis/?ref=gh-tiktok-api) 为准。</sub>
