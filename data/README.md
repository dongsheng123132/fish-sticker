# Data

`species.json` 计划为完整数据集（每条一个物种），**尚未生成**；CSV 为展平子集（尚未生成）。当前仓库仅有样例 `sample.json`。

| 文件 | 内容 | 许可 |
|---|---|---|
| `species.json`（尚未生成） | 除中文图鉴文字外的全部字段 | 编纂部分 MIT；第三方字段沿用各自条款（见 NOTICE.md） |
| `sample.json` | 占坑样例（字段结构演示，待逐项核对） | MIT |

## species.json 字段

| 字段 | 含义 | 来源 | 覆盖 |
|---|---|---|---|
| `id` | `Genus_species`，文件命名的稳定键 | — | 全部 |
| `scientificName` / `authority` | 学名与命名人 | Eschmeyer's Catalog of Fishes | 全部 |
| `taxonomy` | 分类体系、目/科/属 | Eschmeyer's Catalog of Fishes | 全部 |
| `names` | 按语言代码的俗名（en / zh-Hans / zh-Hant / ja …） | FishBase / GBIF / iNaturalist | 待核对 |
| `ids` | wikidata / gbif / fishbase / inaturalist 跨库 ID | 各库 | 待核对 |
| `range` | 生境（marine / freshwater / anadromous）与分布 | FishBase / GBIF | 待核对 |
| `traits` | 体长、体高等形态与生态 | FishBase | 待核对 |
| `conservation` | IUCN 等级、CITES 附录 | IUCN / Wikidata | 待核对 |
| `sticker` | 文件、类型、评分、是否过质量线、许可、参考图来源 | 本项目 | 全部（占坑阶段为 pending） |

## 数据源 / Sources

- Eschmeyer's Catalog of Fishes（加州科学院）
- FishBase <https://www.fishbase.org>
- GBIF <https://www.gbif.org>
- iNaturalist <https://www.inaturalist.org>
- IUCN Red List <https://www.iucnredlist.org>
