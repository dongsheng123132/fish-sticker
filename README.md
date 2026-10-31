# fish-sticker · 全球鱼类贴纸库

全世界现存鱼类的贴纸库：每种一张白边贴纸，附多语言鱼名与分布、形态、保护等级结构化数据。学 [花叔 huashu-bird-sticker](https://github.com/alchaincyf/huashu-bird-sticker) 的「鸣迹」模式，先从**海洋鱼**开始，再补全**淡水鱼**。

> 🚧 **占坑阶段**：数据 schema、许可、样例数据已就位；贴纸尚未生成（筹备中），`data/species.json` 全量数据尚未生成。

**English:** Stickers for the world's fish species — one white-bordered sticker per species, with multilingual names and structured data. Inspired by Huashu's bird stickers. **Early stage: schema, license and samples are live; stickers have not yet been generated (in preparation).**

---

## 这是什么

这是「**鱼迹（Fish Tracks）**」iOS App 的贴纸库。鱼迹是一本贴纸本：你每认出/收藏一种鱼，就把它的贴纸贴进自己的本子里，盖一个日期和地点的邮戳。

全世界现存鱼类约 3.5 万种（海洋鱼约 1.5–2 万种）。我们会分阶段补全：

1. **海洋鱼**（致敬 100 年前的格拉巴图谱，见下文）
2. **淡水鱼**

## 灵感与方法

整套做法照抄花叔的公开方法论（详见他的[长文](https://x.com/AlchainHust/status/2116088319511605472)）：

1. **找参考图**：每种先找一张真实照片（开放许可优先），记录出处、作者、许可。
2. **照着画**：AI 重绘，绝不凭空让模型「凭印象画」。
3. **独立打分审校**：画图和审校分开，独立对辨识特征打分。
4. **画不好就重画**：80 分过线、70–79 保留、<70 重画，`meetsQualityBar` 落字段。

参考图**不打包进仓库**，将逐种在 `data/species.json` 里溯源。

## 数据 schema

每条一个物种（样例见 [`data/sample.json`](data/sample.json)，字段说明见 [`data/README.md`](data/README.md)）：

```json
{
  "id": "Pagrus_major",
  "scientificName": "Pagrus major",
  "authority": "(Temminck & Schlegel, 1843)",
  "taxonomy": { "system": "Eschmeyer's Catalog of Fishes", "order": "Spariformes", "family": "Sparidae", "genus": "Pagrus" },
  "names": { "en": "Red seabream", "zh-Hans": "真鲷", "ja": "マダイ" },
  "ids": { "wikidata": null, "gbif": null, "fishbase": null, "inaturalist": null },
  "range": { "habitat": "marine", "distribution": "Northwest Pacific" },
  "conservation": { "iucn": null },
  "sticker": { "file": null, "kind": "ai-illustration", "reviewScore": null, "meetsQualityBar": false, "license": "PolyForm-Shield-1.0.0", "status": "pending" }
}
```

## 目录结构

```
stickers/<Order>/<Family>/<Genus_species>.webp   贴纸（白边透明底，约 1000px）
data/species.json                                 全量数据（每条一个物种，尚未生成）
data/species.schema.json                          JSON Schema
data/README.md                                    字段说明与来源
LICENSE.md                                        许可概览
NOTICE.md                                         第三方来源说明
```

## 许可

- 贴纸：**PolyForm Shield 1.0.0** —— 源码/资源公开、可复制分发，但**不是 OSI 开源许可**，有**竞争限制**：禁止做与鱼迹竞争的观鱼/识鱼/鱼类图鉴产品。
- 数据（编纂部分）：**MIT**；第三方（分类、鱼名、体征等）在 [NOTICE.md](NOTICE.md) 逐条保留。

详见 [LICENSE.md](LICENSE.md)。

## Roadmap

- [x] 数据 schema 与许可
- [ ] 首批海洋鱼贴纸小样（100–300 种）跑通流水线
- [ ] 海洋鱼全物种（约 1.5–2 万种）
- [ ] 淡水鱼补全
- [ ] 多语言鱼名与跨库 ID 补全
- [ ] 鱼迹 iOS App 上架

## 数据源

- Eschmeyer's Catalog of Fishes（分类权威）
- FishBase（生态、体长、俗名、图片）
- GBIF / iNaturalist（跨库 ID 与分类）
- IUCN Red List（保护等级）

## 致敬格拉巴图谱

鱼迹 App 的复古图鉴页会致敬**格拉巴图谱（グラバー図譜）**——《日本西部及南部鱼类图谱》，仓场富三郎（托马斯·阿尔伯特·格拉巴）于大正初年到昭和初期约 20 年间，请五位长崎画师手绘的 34 卷 805 幅海产鱼类、甲壳类、软体动物图谱，被涩泽敬三誉为「日本四大鱼谱之一」，现藏长崎大学附属图书馆。原作是否已入公有领域需逐作者、逐幅核实（**待核**），不能仅凭年代断言。

## 贡献

发现贴纸错误、鱼名/分类有误、或有更好的开放参考图，欢迎提 issue / PR。观鱼者、鱼类爱好者的纠正是这个项目最宝贵的贡献。
