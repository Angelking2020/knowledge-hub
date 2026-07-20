# 数据集 · PURSUE 第四批（Release 04）

本目录存放对美国战争部 **PURSUE 第四批解密文件**（2026-07-10 发布，共 40 份）的结构化整理结果，供检索、统计与复现分析使用。

## 文件

| 文件 | 说明 |
| --- | --- |
| `pursue-release-04-dataset.json` | 40 条完整记录 + 批次汇总（类型/机构分布、下载 URL） |
| `pursue-release-04-dataset.csv` | 同一数据的表格版，可直接用 Excel / pandas 打开 |
| `DOW-UAP-D092.ocr.txt` | 单份文件 DOW-UAP-D092（蓝皮书审查委员会）PDF 的 OCR 全文（PDF.js 提取，85 页），供 [D092 中译](../DOW-UAP-D092-translation-zh.md)核对 |

## 字段释义（每条 record）

| 字段 | 含义 |
| --- | --- |
| `id` | 文件编号，如 `DOE-UAP-D004`、`DOW-UAP-PR104`（前缀即发布机构） |
| `title` | 官方标题 |
| `type` | 文件类型：`PDF` / `VID`(视频) / `AUD`(音频) / `IMG`(图片) |
| `agency` | 发布机构：Department of War / NASA / CIA / Department of Energy / FBI |
| `incident_date` | 事件发生时间（部分仅有年份） |
| `incident_location` | 事件地点 |
| `featured` | 官方是否标为 Featured（`Yes`/空） |
| `redacted` | 是否含删节（`Yes`/`No`） |
| `description` | **官方 AARO 逐条描述全文**（含 "AARO Comment" 分析注释）——本数据集的核心价值 |
| `source_url` | war.gov 原始文件 URL（视频为 CloudFront/DVIDS 分发） |
| `sha256` | 原始文件的 SHA-256 指纹（来自镜像校验清单，见"来源与可信度"） |
| `size_bytes` | 原始文件字节数 |
| `dvids_video_id` | 视频在 DVIDS 平台的 ID（仅视频有） |

顶层还含：`release_date`、`total_records`、`by_type`、`by_agency`、`documents_zip`、`videos_zip`、`csv_url`。

## 来源与可信度

- **一手来源**：美国战争部官方门户 `war.gov/UFO`（PURSUE 第四批），逐条描述由 AARO 撰写。
- **整理方式**：受采集环境网络策略限制，未直连 war.gov 原始二进制；元数据与描述经以下**相互独立**的开源镜像交叉校验，四者在总量（334）、本批（40）、机构/类型分布上一致：
  - `rizzleroc/pursue-console`（第四批 manifest，含官方描述全文）
  - `BPSAI/pursue-index`（批次差异 + war.gov URL/字节数）
  - `FongShuiLabs/pursueufotracker`（334 份 SHA-256 校验清单）
- **关于 SHA-256**：来自上述镜像的校验清单，用于证明"各镜像对同一份 war.gov 原件的记录一致"；**并非**本项目直连原件独立复算。核验时一切以 `war.gov` 官方原件为准。

## 快速上手

```bash
# 统计（Python）
python3 - <<'PY'
import json, collections
d = json.load(open("pursue-release-04-dataset.json"))
print("总数:", d["total_records"], "| 发布日:", d["release_date"])
print("按类型:", d["by_type"])
print("按机构:", d["by_agency"])
print("含删节:", sum(1 for r in d["records"] if r["redacted"] == "Yes"), "/ 40")
PY

# 表格分析（pandas）
python3 - <<'PY'
import pandas as pd
df = pd.read_csv("pursue-release-04-dataset.csv")
print(df.groupby("agency").size())
print(df[df.redacted == "Yes"].type.value_counts())   # 删节集中在视频
PY
```

完整解读见上一级目录的 [`pursue-release-04-analysis.md`](../pursue-release-04-analysis.md)。
