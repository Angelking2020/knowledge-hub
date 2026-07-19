# 美国第四批 UFO/UAP 解密档案（PURSUE Release 04）下载与分析

> 一句话概括：2026 年 7 月 10 日，美国"战争部"（Department of War）在其官方 UAP 门户 [war.gov/UFO](https://www.war.gov/UFO/) 发布了 **PURSUE 计划第四批解密文件**，共 **40 份**，横跨 **1948–2025 共 77 年**——既有蓝皮书时代的冷战底稿，也有 2025 年黄海上空的红外视频。本文对这 40 份文件做了下载、结构化整理与主题分析。

| 元信息 | 内容 |
| --- | --- |
| 发布方 | 美国战争部（U.S. Department of War）/ AARO（全域异常解析办公室） |
| 计划名称 | **PURSUE** — Presidential Unsealing and Reporting System for UAP Encounters |
| 批次 | 第四批（Release 04） |
| 发布日期 | 2026-07-10 |
| 文件数量 | **40 份**（PDF 14、视频 19、音频 4、图片 3） |
| 数据体量 | 约 **4.44 GB**（音频占 3.4 GB） |
| 官方数据源 | `war.gov/UFO`（含 CSV 清单、文档 zip、视频 zip） |
| 本文整理日期 | 2026-07-14 |
| 本文所用数据 | 官方 AARO 逐条描述 + 结构化元数据，经多个独立开源镜像交叉校验（含 SHA-256），详见[第三节](#三数据从哪来如何下载与核验) |

---

## 速览（TL;DR）

第四批是一次**"补线头"式的定向发布**：规模不大（40 份），但把此前几批留下的历史线索（Project Sign、蓝皮书、绿色火球、核设施异常）系统地补齐、修订、去删节。

**关键数字**

| 维度 | 分布 |
| --- | --- |
| 按类型 | PDF 14 · 视频 19 · 音频 4 · 图片 3 |
| 按机构 | 战争部(DOW) 28 · NASA 7 · CIA 2 · 能源部(DOE) 2 · FBI 1 |
| 按事件年代 | 1940s 4 · 1950s 4 · 1960s 2 · 1970s 4 · 1990s 4 · 2010s 6 · **2020s 16** |
| 删节比例 | **19/40 ≈ 47.5%** 含删节 |

**五条核心发现**

1. **时间跨越 77 年，结论惊人一致**——从 1948 年"确实看到了某物，但无法识别"到 2025 年黄海的"六角星"，官方口径始终是"未解释（unresolved）"，而非"已证实为外星"。
2. **这是一次"平淡化"发布**——大量所谓 UAP 其实指向**已知现象**：宇宙射线在视网膜上的光闪、红外传感器自动增益的伪影、"变形的气球"、圆盘形 VTOL 原型机、流星。**解密 ≠ 证实外星**。
3. **核设施反复出现**——2015 年钻石形物体侵入得州 Pantex 核武器总装厂，与 1949 年 Los Alamos 上空的"绿色火球"遥相呼应，UAP 与核基础设施的关联横跨 66 年。
4. **现代文件几乎必删、历史文件基本不删**——47.5% 的删节几乎全部落在 2015–2025 的军事传感器素材上（保护证人、平台与传感器能力）。
5. **机构分工清晰**——战争部主导现代军事视频，NASA 负责太空视角，CIA/FBI 提供历史情报，能源部对应核设施。

---

## 一、背景：PURSUE 计划与"第四批"是什么

### 1.1 PURSUE 是什么

**PURSUE**（Presidential Unsealing and Reporting System for UAP Encounters，总统解封与 UAP 遭遇报告系统）是美国政府 2026 年启动的跨部门 UAP 解密计划。据官方门户与公开报道，它源于 2026 年 2 月的一项总统指令，要求战争部、FBI、NASA 及情报机构系统识别、审查并公开与 UAP 相关的记录，成果统一发布在 `war.gov/UFO`。

> **UAP** = Unidentified Anomalous Phenomena（不明异常现象）。注意这里是 **A**nomalous（异常）而非早期的 **A**erial（空中）——这一改名来自 2023 财年《国防授权法案》（Inhofe NDAA，2022-12-23 签署），把研究范围从"空中"扩展到海面、水下、太空与"跨介质"（transmedium）观测。

### 1.2 四批发布时间线

PURSUE 采取"滚动发布"，第四批之前已有三批：

| 批次 | 日期 | 规模（约） | 主题侧重 |
| --- | --- | --- | --- |
| Release 01 | 2026-05-08 | 126 PDF + 14 图 + 28 视频 | 首次大规模解密；DOW 任务报告、FBI/NASA/情报机构 |
| Release 02 | 2026-05-22 | 6 PDF + 57 视频 | CIA/DOE/DOW/ODNI 情报记录 + 大批 DoD 视频 |
| Release 03 | 2026-06-12 | 43 PDF + 7 图 + 4 视频 | 蓝皮书、陆海军历史分析、AARO 案卷 |
| **Release 04** | **2026-07-10** | **14 PDF + 3 图 + 19 视频 + 4 音频** | **补齐历史线索 + 现代军事传感器素材** |

四批合计约 **334 份**文件（跨多个独立镜像核对一致）。

### 1.3 与 NARA / AARO 的关系（避免混淆）

同期还有两条相关但不同的"解密轨道"，容易混淆：

- **war.gov/UFO（PURSUE）**：战争部主导的主动解密门户，即本文对象。
- **NARA "UAP 记录集"（Record Group 615）**：国家档案馆依 2024 财年 NDAA 第 1841–1843 条接收 ODNI/OSD/FAA/NRC 移交的记录，提供 zip + JSON 元数据批量下载。
- **AARO 官网（aaro.mil）**：全域异常解析办公室的案卷与信息文件。

本文只分析 **PURSUE 第四批**；PURSUE 的逐条描述本身就出自 AARO。

---

## 二、第四批数据总览（40 份文件）

### 2.1 按类型

| 类型 | 数量 | 体量 | 说明 |
| --- | --- | --- | --- |
| PDF 文档 | 14 | ~234 MB | 历史研究、情报备忘、海军 Range Fouler 表格 |
| 视频 VID | 19 | ~797 MB | 红外/光电传感器拍摄的"未解 UAP 报告" |
| 音频 AUD | 4 | **~3.4 GB** | Apollo 14/17 任务后汇报录音（体量最大） |
| 图片 IMG | 3 | ~4 MB | NASA STS-80 近地轨道三连拍 |

> 有意思的是：**体量前三名全是 NASA 音频**——NASA-UAP-D026（Apollo 14 汇报，1.42 GB）、D028（Apollo 17，827 MB）、D029（600 MB）。真正"信息密度高"的往往是几百 KB 的 PDF。

### 2.2 按机构

| 机构 | 数量 | 主要内容 |
| --- | --- | --- |
| 战争部 DOW | 28 | 现代军事视频 + 蓝皮书/Project Sign 历史文档 |
| NASA | 7 | STS-80 图片 3 + Apollo 音频 4 |
| CIA | 2 | 1955 年"非常规飞行器"备忘与分析 |
| 能源部 DOE | 2 | 1949 Los Alamos 会议 + 2015 Pantex 核厂事件 |
| FBI | 1 | 1967/1974 年 UFO 相关信件 |

### 2.3 按事件年代与地理

事件年代呈"两头重"：一头是 **1948–1955 的冷战早期**（10 份），一头是 **2015–2025 的现代军事遭遇**（22 份）。

| 年代 | 数量 |
| --- | --- |
| 1940s | 4 |
| 1950s | 4 |
| 1960s | 2 |
| 1970s | 4 |
| 1990s | 4 |
| 2010s | 6 |
| **2020s** | **16** |

地理上，现代素材集中在**西太平洋**（黄海、东海、南海）与**美国本土东/西海岸**及大西洋：美东 8、"多地/Various" 5、得州 5、东海 3、近地轨道 3、大西洋 3、弗吉尼亚 2、黄海 2、美西 2、中东 2，另有新墨西哥、墨西哥湾、阿塞拜疆、南海各 1。

### 2.4 删节情况

**19/40（约 47.5%）**文件含删节。关键规律：**删节几乎全部落在 2015–2025 的军事传感器素材上**（保护证人身份、平台与传感器能力），而 1948–1967 的历史文档基本不删。

---

## 三、数据从哪来、如何下载与核验

### 3.1 官方数据源

第四批的官方入口是 `war.gov/UFO`，其分发结构为：

- **CSV 清单**：`https://www.war.gov/Portals/1/Interactive/2026/UFO/uap-data.csv?release=4`
- **文档包（zip）**：`https://www.war.gov/medialink/ufo/071026/release_04/release_04_documents_071026.zip`
- **视频包（zip）**：`https://d34w7g4gy10iej.cloudfront.net/release_04/uap_release04_videos_071026.zip`
- **单份文件**：`https://www.war.gov/medialink/ufo/071026/release_04/documents/<文件名>.pdf`
  （`071026` 即 07/10/26 发布日）

### 3.2 本文的数据获取方式（诚实说明）

本次分析在一个**受网络策略限制的环境**中完成，`war.gov` 与其 CloudFront CDN 的原始二进制**无法直连**。因此我采取的路径是：

1. **下载并整合权威结构化元数据 + 官方 AARO 逐条描述**（每份文件的标题、机构、事件时间地点、删节标记、以及 AARO 亲自撰写的"描述"与"AARO Comment"分析注释）；
2. **用多个相互独立的开源镜像交叉校验**，确保清单完整、计数一致、且每份文件都带 **SHA-256** 指纹。

用于交叉校验的独立镜像（均可在 GitHub 直接访问）：

| 镜像仓库 | 提供的数据 |
| --- | --- |
| `rizzleroc/pursue-console` | 第四批完整 manifest（含官方描述全文） |
| `BPSAI/pursue-index` | 批次差异（tranche-diff）+ 每份文件的 war.gov URL 与字节大小 |
| `FongShuiLabs/pursueufotracker` | 334 份文件的 SHA-256 校验清单、时间线 JSON |

**可信度评估**：四个独立来源在"总量 334、本批 40、按机构/类型分布"上**完全一致**，且每份文件都有 SHA-256 与字节数——这为"清单本身没有被篡改或遗漏"提供了强证据。需要提醒的是，**SHA-256 来自第三方镜像**（我无法直连原件独立复算），因此它证明的是"各镜像对同一份 war.gov 原件的记录一致"，一切仍以 `war.gov` 官方原件为准。

### 3.3 本仓库附带的数据集

整理后的结构化数据集已放在同目录 [`data/`](data/) 下：

- [`data/pursue-release-04-dataset.json`](data/pursue-release-04-dataset.json)：40 条完整记录（含官方描述、SHA-256、源 URL）
- [`data/pursue-release-04-dataset.csv`](data/pursue-release-04-dataset.csv)：同一数据的表格版，便于 Excel/pandas 分析

字段释义与自助核验命令见 [`data/README.md`](data/README.md)。

---

## 四、四大主题深度解读

40 份文件可归为四条清晰的主题线。

### 4.1 冷战早期的历史底稿（1948–1967，约 14 份）

第四批把美国政府**最早期**的 UFO 研究文档大量补齐：

- **Project Sign 进度报告（1948，`DOW-UAP-D097`）**：美国空军航空器材司令部关于 Project Sign（1948–1949 首个官方 UFO 调查计划）的初期报告，收录 **1947–1948 年 100 起目击**。文件里还夹着一篇发表于航空杂志《The Aeroplane》的趣文《飞碟的生物学》（*The Biology of the Flying Saucer*）。
- **"飞行物事件分析"第 203 号研究（`DOW-UAP-D093` / `D094`）**：空军航空情报处的同一份研究，本批同时给出 **1948-12-10 的早期草稿**与 **1949-04-28 的修订版**（AARO 明确注释二者"实质相似，系草稿与修订关系"）。其核心结论极具代表性：

  > "看来确实有某个物体被看到了；然而无法轻易识别它是什么。"
  > 研究给出两种"合理"来源——本国或外国技术；并建议**若属外国，应审慎假设 UFO 观测源于苏联的科学/军事/情报活动**并认真对待其威胁。

  文件甚至附上"飞翼"（flying wing）实验机型的平面图，试图解释某些常见的 UFO 外形。

- **绿色火球与 Los Alamos 1949 会议（`DOE-UAP-D004`）**：1949 年在 Los Alamos 科学实验室（今 Los Alamos 国家实验室）召开的一次会议记录，与会者包括多位曾参与曼哈顿计划的顶尖物理学家。议题是解释数月来在实验室上空反复出现的"绿色火球"。**会议未达成共识**：主流假设是"浅角度、高空进入大气的流星"；爱德华·特勒（Edward Teller）提出若非"实体"，也可能是某种"电子现象"；而流星学专家 Lincoln LaPaz 则表示"就我所知，陨石坠落从未观察到这样的现象"。

- **CIA 1955：参议员 Russell 的苏联目击（`CIA-UAP-D020` / `D021`）**：一份 CIA 汇报记录了 4 人（含美国参议员 **Richard Russell**、一名军人、两名政府官员）1955 年在苏联境内（今阿塞拜疆、Baku 与 Tbilisi 之间）**乘火车时**目击"绿黄色"发光"飞碟/非常规飞行器"。CIA 结论："大概可以解释为陡爬升的飞机或导弹"，"证据尚不足以断定苏联已研制出全新类型的飞行器"。配套分析（D021）还援引了 **1953 年 Robertson 专家组**"几乎所有目击都不构成对美国的威胁"的结论，并提到当时美加联合的"Project Y"圆盘形飞行器研究。

- **美加联合航空项目与 VTOL（`DOW-UAP-D095`，1954–1955）**：这份 32 MB 的文件是"平淡解释"的典型——它评估了 **Avro Project Y2**（美加联合研制的近圆盘形垂直起降机），并在 1954 年备忘里直言：**圆盘形 VTOL 对不熟悉该技术的观察者而言，很容易被误认为 UFO**，建议重新审视苏军活动附近的 UFO 报告是否其实是未知的外国先进 VTOL。同一文件也承认，1955 年 7 月纽芬兰附近一架空军 KC-97 的遭遇"地面雷达回波与机组目视同时出现，委员会无法解释"。此外还涉及用流星雷达数据改进 AN/FPS-17 雷达、以及美加 **CIRVIS** 联合上报机制。

- **蓝皮书相关（`DOW-UAP-D096` 通信 / `DOW-UAP-D092` 审查委员会）**：D096（126 MB）是围绕 Project Blue Book（1952–1969）的大量往来信件；**D092 尤其重要**——1966–1967 年空军科学咨询委员会审查蓝皮书的特设委员会记录，其建议"委托高校科学团队调查选定的 UFO 目击"被空军采纳，**这直接促成了随后委托科罗拉多大学开展的"康登委员会"研究（1966–1968），其 1968 年报告最终导致 1969 年蓝皮书计划关闭**。（该文件已全文中译，另见 [DOW-UAP-D092 逐页翻译与导读](DOW-UAP-D092-translation-zh.md)——它内部还完整附带了 1953 年 CIA"罗伯逊专家组"报告。）

- **FBI 信件（`FBI-UAP-D014`，1967/1974）**：两封信。1967 年一封转述一名 11 岁儿童"听到怪声、看到闪光"的经历；1974 年 FBI 回复 Larry Bryant 关于"1954 年一起载人 UFO 目击"的查询时明确表示：**局里没有此类记录，且截至 1974 年 FBI 不再收集 UFO 目击信息**。

> **主题小结**：这批历史档案揭示了两点——① 冷战语境下，美国政府的第一反应是"这会不会是苏联的先进技术？"；② 政府长期处于一种"确实看到了、但无法确证"的状态，且**很早就倾向于用流星、实验机型等平淡原因来解释**。

### 4.2 现代军事遭遇：传感器视频与 Range Fouler（2015–2025，约 22 份）

这是第四批数量最多、也最"神秘"的部分——一批标题为 **"Unresolved UAP Report"（未解 UAP 报告）**的红外/光电视频，由印太司令部（INDOPACOM）、北方司令部（NORTHCOM）、中央司令部（CENTCOM）、海军、空军等提交给 AARO。

- **地理热点**：西太平洋（黄海、东海、南海）+ 美国东/西海岸 + 大西洋 + 中东。这与当下的军事关注区域高度重合。
- **黄海"六角星"（`DOW-UAP-PR104`，2025）**：本批最"出圈"的画面——印太司令部提交的 **18 秒红外视频**，传感器追踪一个"形似六角星的对比区域"。官方描述刻意中性，并附免责声明"不应被解读为任何分析结论"。
- **海军 Range Fouler Debrief（配对文档 + 视频）**：Range Fouler 是海军用于记录"训练/作战空域被非授权闯入"的标准表格，本批有三组文档与视频配对，细节生动：
  - `DOW-UAP-D089` ↔ 视频 `PR106`（美东 2020）：物体"相当小"、沿恒定方向移动、外形"无法分辨"、**金属质感、底部反光**。
  - `DOW-UAP-D090` ↔ 视频 `PR112`（美东 2019）：5 名人员目击，飞行员称其"具有我在空军和海军服役 **28 年从未见过**的飞行特征"；值得注意的是，这段视频**拍自一架民用飞机**。
  - `DOW-UAP-D091` ↔ 视频 `PR116`（大西洋 2020）："较深的栗色、约 12–15 英尺高、随风飘移、不机动、像一个**大而略微变形的气球**"。
- **AARO 的"降温"注释**：官方并不回避平淡解释。例如对墨西哥湾 2019 视频（`PR115`），AARO 直接注明：**红外系统在目标温度与环境相近时，会因自动增益（auto-gain）调整而"融入背景或看似闪烁"**。多段来自海军 UAPTF 的旧素材还标注"当时无正式数据留存规范、且在上报前曾被数字修改"。

> **主题小结**：现代部分几乎**全部带删节**，且官方叙述极其克制——只客观描述"传感器画面里发生了什么"，反复声明"不构成对事件真实性/性质/意义的判断"。这是一种典型的"透明但不背书"的姿态。

### 4.3 NASA 的太空视角（1971–1996，共 10 份）

- **STS-80 三连拍（`NASA-UAP-D030/031/032`，1996）**：1996 年 11–12 月，哥伦比亚号航天飞机上的宇航员拍下一个近地轨道不明物体的三张连续照片。官方描述本身就暗示了"平淡"解读：第二张里物体"**沿主轴翻滚，符合自由漂浮物体的行为**"，第三张显示它"沿轨迹从哥伦比亚号与地球之间穿过"——即很可能是脱落碎片/冰晶一类的自由漂浮物。
- **Apollo 14/17 "光闪现象"音频（`NASA-UAP-D026–D029`，1971/1972）**：四段任务后汇报录音，讨论宇航员报告的"光闪现象"（light flash phenomena）。**这其实是一个早已被科学解释的生理现象**——高能宇宙射线穿过眼球击中视网膜，产生光条/闪光的知觉。Apollo 17 三名乘员中有两人在环月轨道乃至月面都报告过。

> **主题小结**：NASA 部分体现的是"透明度优先"——**连早已有明确科学解释的现象（视网膜光闪、轨道漂浮物）也一并纳入 UAP 档案公开**。这也提醒读者：档案里的"unidentified"很多时候只是"当年记录时未归类"，而非"至今无法解释"。

### 4.4 核安全联结：反复出现的"核设施上空异常"（1949 & 2015）

这条线索虽然文件不多，却最具"国安分量"：

- **Pantex 核厂入侵（`DOE-UAP-D005`，2015）**：2015 年 9 月 1 日，一个不明物体侵入得州 Amarillo 附近 **Pantex 工厂**上空。Pantex 是美国核武器**总装、拆解、维护与延寿**的主要设施，属最敏感的国安场所之一。本批给出的是比 5 月 22 日（第二批 `DOE-UAP-D001`）**删节更少的更完整版本**——这是一个"分批降低删节度、逐步放开"的清晰例子。
- **与 1949 绿色火球呼应**：早在 1949 年，Los Alamos（同为核心核设施）上空就反复出现"绿色火球"（见 4.1）。**UAP 与核基础设施的关联横跨 66 年**，是解密叙事里反复出现、也最受研究者关注的模式之一。

> **主题小结**：无论最终解释是什么，"异常现象偏好出现在核设施上空"这一**统计学观感**，是历届 UAP 调查（从 Project Sign 到 AARO）都无法回避的线索。

---

## 五、关键案例卡片

### 🛰️ 案例一：黄海"六角星"（2025）
- **文件**：`DOW-UAP-PR104`（视频，18 秒，红外）
- **来源**：印太司令部 → AARO
- **画面**：传感器追踪一个"形似六角星"的高对比区域，全程居中。
- **官方口径**：仅客观描述画面，附"不构成任何分析结论"的免责声明。
- **为何重要**：地点敏感（黄海）、形态奇特、且是 2025 年的**近期**素材，是本批传播度最高的画面。
- **审慎解读**：红外"星芒"常见于点状热源的传感器光学效应；官方未给出结论，读者亦不宜过度解读。

### ☢️ 案例二：Pantex 核厂入侵（2015）
- **文件**：`DOE-UAP-D005`（PDF，含图像与报告）
- **画面/事件**：钻石形不明物体侵入核武器总装厂空域。
- **看点**：本批是**去删节的更完整版**（对比 5/22 的 D001）。
- **为何重要**：直接触及"UAP × 核安全"这一最敏感交叉点。

### 🟢 案例三：绿色火球 / Los Alamos 会议（1949）
- **文件**：`DOE-UAP-D004`（PDF，会议记录）
- **人物**：Edward Teller、Lincoln LaPaz 等曼哈顿计划科学家。
- **结论**：未达共识；主流假设为"浅角度高空流星"。
- **为何重要**：**最早**由顶尖物理学家正式讨论 UAP 的原始记录之一，与 2015 Pantex 构成核设施异常的"历史闭环"。

### 🚂 案例四：参议员 Russell 的苏联目击（1955）
- **文件**：`CIA-UAP-D020` / `D021`
- **事件**：美国参议员 Richard Russell 一行在苏联乘火车目击"绿黄色"发光物。
- **CIA 结论**："大概是陡爬升的飞机或导弹"，证据不足以断定苏联新机型。
- **为何重要**：高级别政要 + 冷战情报语境，且展示了 CIA 的"平淡化"分析范式（含 Robertson 专家组、Project Y）。

---

## 六、横向观察与模式

把 40 份文件放在一起看，会浮现几条贯穿性的规律：

1. **77 年，同一句话**。从 1948 年的"看到了某物、无法识别"到 2025 年黄海的"未解报告"，官方结论的**语气几乎没变**：承认现象、拒绝下定论、避免背书任何解释。
2. **"解密"不等于"证实外星"**。本批相当比例的内容其实指向**已知或高度可能的平淡原因**：视网膜光闪（宇宙射线）、红外自动增益伪影、"变形的气球"、圆盘形 VTOL 原型、流星。真正"仍然无法解释"的是少数。
3. **删节的边界即"敏感度"的边界**。47.5% 的删节几乎全落在 2015–2025 的军事传感器素材上（证人、平台、传感器能力），历史文档则近乎全公开——删的不是"真相"，而是**现役能力**。
4. **机构分工映射议题分工**：DOW = 现代军事视频；NASA = 太空；CIA/FBI = 历史情报；DOE = 核设施。想研究某一议题，可直接按机构前缀检索（`DOW-`/`NASA-`/`CIA-`/`FBI-`/`DOE-`）。
5. **"补线头"式发布**。第四批大量是对前几批的**补充与修订**：D093/D094 同一研究的草稿与修订并置、Pantex D005 是 D001 的去删节版、多段视频与 Range Fouler 文档互相配对。这更像"把悬着的线索系紧"，而非抛出全新爆点。
6. **数据治理本身在进步**。旧素材反复标注"当年无正式留存规范、曾被数字修改"，与今天标准化的 AARO 上报/描述流程形成对照——这也是解密的**副产品价值**：它记录了政府 UAP 数据管理**从混乱到规范**的演变。

---

## 七、如何自己下载与核验

```bash
# 1) 直接用本仓库整理好的数据集（推荐，无需访问 war.gov）
#    - notes/ufo-uap-declassification/data/pursue-release-04-dataset.json
#    - notes/ufo-uap-declassification/data/pursue-release-04-dataset.csv

# 2) 从官方 war.gov 下载原始文件（需能访问 war.gov / CloudFront）
#    官方 CSV 清单：
curl -L "https://www.war.gov/Portals/1/Interactive/2026/UFO/uap-data.csv?release=4" -o release_04.csv
#    单份 PDF（示例：1949 Los Alamos 会议）：
curl -L "https://www.war.gov/medialink/ufo/071026/release_04/documents/DOE-UAP-D004_Los-Alamos-Conference-on-Aerial-Phenomena_1949.pdf" -o D004.pdf

# 3) 用数据集里的 SHA-256 核验下载到的原件是否一致
sha256sum D004.pdf
#    再与 data/pursue-release-04-dataset.json 中对应记录的 sha256 字段比对
python3 - <<'PY'
import json
d = json.load(open("notes/ufo-uap-declassification/data/pursue-release-04-dataset.json"))
rec = next(r for r in d["records"] if r["id"] == "DOE-UAP-D004")
print("expected sha256:", rec["sha256"])
print("size (bytes):   ", rec["size_bytes"])
PY
```

---

## 八、局限与免责声明

- **数据来源**：本文分析基于**官方 AARO 逐条描述 + 结构化元数据**，并以多个第三方开源镜像交叉校验；受本环境网络策略限制，**未直连 war.gov 的原始二进制文件**。SHA-256 来自镜像方，用于"镜像间一致性"证明，一切以 war.gov 官方原件为准。
- **官方描述的性质**：war.gov 对每段视频都附有"仅供参考、**不构成对事件真实性/性质/意义的分析判断**"的免责声明。本文引用时保留了这一语境。
- **"Unresolved / Unidentified" 的含义**：意为"（暂）未解释"，**不等于**"外星"或"超自然"。多份文件的官方描述本身就指向平淡解释。
- **数据可能变动**：war.gov 会滚动更新，第四批的视频包在发布初期一度为空、随后补齐；本文数据整理于 2026-07-14，后续如有增补以官方为准。

---

## 参考来源

**官方**
- [Presidential Unsealing and Reporting System for UAP Encounters (PURSUE) — war.gov/UFO](https://www.war.gov/ufo/)
- [Department of War Releases UAP Files in Historic Transparency Effort（第一批新闻稿）](https://www.war.gov/News/Releases/Release/Article/4480582/)
- [United States UFO files — Wikipedia](https://en.wikipedia.org/wiki/United_States_UFO_files)

**新闻报道（第四批）**
- [The Hill — Pentagon releases fourth batch of UFO files: What to know](https://thehill.com/homenews/administration/5962825-pentagon-releases-fourth-batch-of-ufo-files/)
- [NewsNation — Pentagon releases fourth batch of UFO files](https://www.newsnationnow.com/space/ufo/pentagon-ufo-files-fourth-release/)
- [Christian Post — Pentagon releases fourth batch of UFO files: 'Unlike anything I had seen'](https://www.christianpost.com/news/pentagon-releases-fourth-batch-of-ufo-files.html)

**用于交叉校验的开源镜像 / 数据集（GitHub）**
- [rizzleroc/pursue-console](https://github.com/rizzleroc/pursue-console) — 第四批 manifest（含官方描述全文）
- [BPSAI/pursue-index](https://github.com/BPSAI/pursue-index) — 批次差异与 war.gov URL/字节大小
- [FongShuiLabs/pursueufotracker](https://github.com/FongShuiLabs/pursueufotracker) — 334 份文件 SHA-256 校验清单
- [Co-Messi/uap-pursue](https://github.com/Co-Messi/uap-pursue) — Releases 01–04 完整归档索引

---

## 附录 A：第四批 40 份文件完整清单

图例：★ = 官方标为 Featured；🔒 = 含删节。

| # | ID | 类型 | 机构 | 事件时间 | 地点 | 标记 | 标题 |
|---|---|---|---|---|---|---|---|
| 1 | DOE-UAP-D004 | PDF | DOE | 1949 | 新墨西哥 | ★ | Los Alamos 空中现象会议（绿色火球） |
| 2 | DOW-UAP-D094 | PDF | DOW | 1949-04 | 弗吉尼亚 | ★ | 飞行物事件分析 No.203（修订版） |
| 3 | DOW-UAP-D097 | PDF | DOW | 1948 | 多地 | ★ | Project Sign 进度报告（100 起目击） |
| 4 | DOW-UAP-PR104 | VID | DOW | 2025 | 黄海 | ★🔒 | 未解 UAP 报告——"六角星" |
| 5 | DOW-UAP-PR105 | VID | DOW | 2025 | 东海 | ★🔒 | 未解 UAP 报告（5 分钟红外） |
| 6 | DOW-UAP-PR113 | VID | DOW | 1996 | 美西 | ★🔒 | 未解 UAP 报告（UAPTF 旧素材） |
| 7 | DOW-UAP-PR115 | VID | DOW | 2019 | 墨西哥湾 | ★🔒 | 未解 UAP 报告（8 秒，AARO 注:自动增益） |
| 8 | NASA-UAP-D030 | IMG | NASA | 1996 | 近地轨道 | ★ | STS-80 不明物体 图 1 |
| 9 | NASA-UAP-D031 | IMG | NASA | 1996 | 近地轨道 | ★ | STS-80 不明物体 图 2（翻滚） |
| 10 | NASA-UAP-D032 | IMG | NASA | 1996 | 近地轨道 | ★ | STS-80 不明物体 图 3 |
| 11 | CIA-UAP-D020 | PDF | CIA | 1955 | 阿塞拜疆 | | 非常规飞行器目击备忘（参议员 Russell） |
| 12 | CIA-UAP-D021 | PDF | CIA | 1955 | — | 🔒 | 非常规飞行器目击分析 |
| 13 | DOE-UAP-D005 | PDF | DOE | 2015-09 | 得州 | 🔒 | Pantex 核厂不明物体事件报告 |
| 14 | DOW-UAP-D089 | PDF | DOW | 2020 | 美东 | 🔒 | Range Fouler 报告（配 PR106） |
| 15 | DOW-UAP-D090 | PDF | DOW | 2019 | 美东 | 🔒 | Range Fouler 报告（"28 年未见"，配 PR112） |
| 16 | DOW-UAP-D091 | PDF | DOW | 2020 | 大西洋 | 🔒 | Range Fouler 报告（"变形气球"，配 PR116） |
| 17 | DOW-UAP-D092 | PDF | DOW | 1966-67 | 多地 | | 空军审查蓝皮书委员会（→ 康登委员会） |
| 18 | DOW-UAP-D093 | PDF | DOW | 1948-12 | 弗吉尼亚 | | 飞行物事件分析 No.203（草稿版） |
| 19 | DOW-UAP-D095 | PDF | DOW | 1954-55 | 多地 | | 美加航空项目与 VTOL（Avro Project Y2） |
| 20 | DOW-UAP-D096 | PDF | DOW | 1955 | 多地 | | 蓝皮书相关往来信件（126 MB） |
| 21 | DOW-UAP-PR024 | VID | DOW | 2023 | 中东 | | 未解 UAP 报告（CENTCOM） |
| 22 | DOW-UAP-PR030 | VID | DOW | 2023 | 中东 | 🔒 | 未解 UAP 报告（CENTCOM） |
| 23 | DOW-UAP-PR100 | VID | DOW | 2023 | 黄海 | 🔒 | 未解 UAP 报告（4:57，光电+红外） |
| 24 | DOW-UAP-PR101 | VID | DOW | 2024 | 南海 | 🔒 | 未解 UAP 报告（"一列"对比区域） |
| 25 | DOW-UAP-PR102 | VID | DOW | 2024 | 东海 | 🔒 | 未解 UAP 报告（36 秒） |
| 26 | DOW-UAP-PR103 | VID | DOW | 2024 | 东海 | 🔒 | 未解 UAP 报告（自动追踪） |
| 27 | DOW-UAP-PR106 | VID | DOW | 2020 | 美东 | | 未解 UAP 报告（配 D089） |
| 28 | DOW-UAP-PR107 | VID | DOW | 2020 | 美东 | 🔒 | 未解 UAP 报告（NORTHCOM） |
| 29 | DOW-UAP-PR108 | VID | DOW | 2020 | 美西 | | 未解 UAP 报告（2:16） |
| 30 | DOW-UAP-PR109 | VID | DOW | 2015 | 美东 | | 未解 UAP 报告（UAPTF 旧素材） |
| 31 | DOW-UAP-PR110 | VID | DOW | 2020 | 美东 | | 未解 UAP 报告（27 秒） |
| 32 | DOW-UAP-PR111 | VID | DOW | 2020 | 美东 | 🔒 | 未解 UAP 报告（多对比区域） |
| 33 | DOW-UAP-PR112 | VID | DOW | 2019 | 美东 | 🔒 | 未解 UAP 报告（民用机拍摄，配 D090） |
| 34 | DOW-UAP-PR114 | VID | DOW | 2016 | 大西洋 | 🔒 | 未解 UAP 报告（39 秒） |
| 35 | DOW-UAP-PR116 | VID | DOW | 2020 | 大西洋 | 🔒 | 未解 UAP 报告（配 D091） |
| 36 | FBI-UAP-D014 | PDF | FBI | 1967/1974 | 多地 | | UFO 目击相关信件 |
| 37 | NASA-UAP-D026 | AUD | NASA | 1971 | 得州 | | Apollo 14 汇报（光闪现象，1.42 GB） |
| 38 | NASA-UAP-D027 | AUD | NASA | 1971 | 得州 | | Apollo 14 汇报（续） |
| 39 | NASA-UAP-D028 | AUD | NASA | 1972 | 得州 | | Apollo 17 医疗汇报（光闪现象） |
| 40 | NASA-UAP-D029 | AUD | NASA | 1972 | 得州 | | Apollo 17 医疗汇报（续） |

> 完整字段（官方描述全文、SHA-256、源 URL、字节数）见 [`data/pursue-release-04-dataset.json`](data/pursue-release-04-dataset.json)。

---

*本文为学习/研究/公共记录用途整理，采用仓库统一的 [CC BY 4.0](../../LICENSE) 许可。内容力求忠实于官方描述与可核验的元数据；如与 war.gov 官方原件有出入，以官方为准。*
