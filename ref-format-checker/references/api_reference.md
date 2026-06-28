# 参考文献格式检查器 — 参考手册

## 一、DOI 错配案例库 🔴

以下案例均来自真实审读实践。**DOI 四要素（作者/标题/刊名/DOI）中任一项与解析结果不一致，均为一级问题——比所有格式错误加起来都严重。格式错了可以改，文献引用张冠李戴是学术诚信问题。**

每种模式附带诊断特征，帮助在批量审读时快速识别。

### 快速分诊清单（优先级排序，非选择性过滤）

**含 DOI 的文献必须 100% 逐条核验。** 下表仅用于决定核验的先后顺序，不提供跳过任何条目的依据。

逐条扫描参考文献时，根据以下信号确定核验优先级：

| 信号 | 应触发的检查 | 风险 |
|------|------------|------|
| 第一作者看不出中文姓氏（华人团队论文） | DOI 核验真实作者名 | 🔴 姓名可能全错 |
| 标题关键词与论文主题无交集 | DOI 核验真实标题 + 主题相关性 | 🔴 可能是无关文献 |
| 刊名使用全称（非 PubMed 缩写） | DOI 核验真实刊名 | 🟡 刊名可能写错 |
| DOI 后缀格式异常（如 `0012`、`07.0`、`.0`） | DOI 有效性验证 | 🟡 DOI 可能抄错 |
| 英文翻译行数据与中文条目不一致 | 逐字段对照 | 🟡 卷期页码可能复制自相邻文献 |
| 无 DOI | 标记"未经核验"，建议补充 | 🟡 无法验证 |

**分诊原则：宁可多核验，不可漏一条。核验一条正确的 DOI 只需 30 秒，漏掉一条张冠李戴的文献代价是审稿人信任。分诊排序不等同于选择性核验——所有条目最终都必须核验。**

### 模式 A："张冠李戴" — DOI 正确，作者/标题是另一篇论文

**案例 A1：**
```
DOI: 10.1111/jocn.16421

稿件文献：Tayyib N, Coyer F, Lewis P. Effectiveness of nurse-led versus
          multidisciplinary team models in pressure injury healing[J].
          J Clin Nurs, 2023, 32(5-6):712-726.

DOI 实际：Artola M, Hernando A, Vidal O, et al. The role of specialist
          nurses in detecting spasticity and related symptoms in multiple
          sclerosis[J]. J Clin Nurs, 2023, 32(13-14):3496-3503.

结论：稿件中的作者/标题与 DOI 完全不符。稿件声称的 Tayyib 论文可能
      真实存在但使用了错误的 DOI，或根本不存在。需要：
      1. 在 PubMed/CrossRef 中检索 Tayyib N + pressure injury
      2. 确认该论文的真实 DOI
      3. 替换为正确的作者/标题/DOI 组合
```

**案例 A2：**
```
DOI: 10.1186/s12893-024-02579-w

稿件原文（旧版）：Wang Y, Xiang L, Luo Y, et al. Evidence summary on
                  nutrition management for post-stroke dysphagia[J].
                  Am J Transl Res, 2022, 14(11):8252-8262.

DOI 实际指向：BMC Surgery 期刊。经核实，正确文献为：
              Liu G, Xiao L, Zhou X, et al. Summary of the best evidence
              for the safe use of pneumatic tourniquet in limb surgery[J].
              BMC Surg, 2024, 24(1):281.

结论：稿件作者/标题/刊名全错，DOI 指向 BMC Surgery 而非 Am J Transl Res。
```

### 模式 B："偷梁换柱" — DOI 正确，但刊名/卷期全错

**案例 B1：**
```
稿件文献：Brouwers MC, Kho ME, Browman GP, et al. AGREEⅡ: advancing
          guideline development, reporting and evaluation in health care[J].
          Canadian Medical Association Journal, 2010, 182(18):E839-E842.
          DOI: 10.1503/cmaj.090449

DOI 实际：10.1016/j.jclinepi.2010.07.001 → J Clin Epidemiol, 2010,
          63(12):1308-1311

正确引用：Brouwers MC, Kho ME, Browman GP, et al. AGREE Ⅱ: advancing
          guideline development, reporting and evaluation in health care[J].
          J Clin Epidemiol, 2010, 63(12):1308-1311.
          DOI: 10.1016/j.jclinepi.2010.07.001

教训：AGREE II 最初在 CMAJ 发表，但 2010 年正式版本发表在 J Clin Epidemiol。
      稿件引用的 DOI 也指向另一篇 CMAJ 文章。必须通过 DOI 核验确认最终出处。
```

### 模式 C："狸猫换太子" — DOI 指向同一期刊的不同论文

**案例 C1：**
```
DOI: 10.1111/wrr.12921

稿件文献：Smet S, Lahousse A, Van Damme N, et al. Comparison of instruments
          for measuring pressure ulcer healing[J]. Wound Repair Regen, 2021,
          29(4):635-647.

DOI 实际：2021 WHS Abstract Session List Key[J]. Wound Repair Regen, 2021,
          29(3):A1-A53.

结论：DOI 指向 WHS 会议摘要集，不是 Smet 的论文。需要在 Wound Repair Regen
      中重新检索 Smet 的压力性损伤愈合评估工具论文的正确 DOI。
```

### 模式 D："风马牛不相及" — 文献主题与论文完全无关

**案例 D1：**
```
DOI: 10.1111/jce.16255

稿件文献：Kazawa S, et al. Feasibility of a novel atrial mechanical sensing
          method for leadless atrioventricular synchronous pacing[J].
          J Cardiovasc Electrophysiol, 2024, 35(6):1115-1120.

论文主题：社区居家失能老人压力性损伤护理

结论：心脏起搏器论文出现在压力性损伤护理共识中，完全无关。极可能是：
      1. 文献管理软件（EndNote/Zotero）导入时编号错乱
      2. 参考文献在多次修改中被错误替换
      3. 需核实后删除或替换为相关文献
```

**案例 D2：**
```
DOI: 10.1111/jocn.16421（同模式 A 案例 A1）

稿件文献：Artola M, et al. The role of specialist nurses in detecting
          spasticity and related symptoms in multiple sclerosis[J].

论文主题：压力性损伤护理

结论：多发性硬化症相关论文，与压力性损伤无关，需替换。
```

---

## 二、参考文献核验自动化策略

### 核验原则

**DOI 是核验参考文献的手段之一，不是唯一手段。最终目标是确认稿件中的每一条参考文献真实存在且信息（作者/标题/刊名/卷期页码）准确无误。**

- 有 DOI ≠ 引用正确（DOI 可能指向完全不同的论文）
- 无 DOI ≠ 无法核验（可通过标题/作者在多数据库中检索确认）
- 每条参考文献至少通过一个渠道核验通过，方可标记为"已核验"

### 核验渠道总览

按效率和覆盖面排序，对每条参考文献，依次尝试以下渠道。任一渠道核验通过即确认该条文献数据正确：

| 渠道 | 适用条件 | 方式 | 覆盖面 |
|------|---------|------|--------|
| 渠道 1：DOI 解析 | 有 DOI | doi.org API / CrossRef API | CrossRef 注册的国际 DOI |
| 渠道 2：学术数据库标题检索 | 不限 | PubMed / OpenAlex / Semantic Scholar API | 有英文标题/摘要的文献 |
| 渠道 3：WebSearch 多搜索词并行 | 不限 | Google / Bing / 百度学术 | 中英文文献全覆盖 |
| 渠道 4：CNKI DOI 结构分析 | CNKI/ISTIC DOI | 正则解析 DOI 后缀 | CNKI 注册的中文文献 |
| 渠道 5：人工核验 | 渠道 1-4 均失败 | 万方 / 知网 / 维普 | 中文文献终极兜底 |

**核验流程决策树：**
```
拿到一条参考文献
  ├── 有 DOI？
  │     ├── 是 → 渠道 1（DOI 解析）
  │     │         ├── 解析成功 → 四要素比对 → 通过/标记差异
  │     │         └── 解析失败（CNKI DOI / Cloudflare）→ 渠道 2-5
  │     └── 否 → 直接进入渠道 2-5
  │
  └── 渠道 2（学术数据库标题检索）
        ├── PubMed / OpenAlex / Semantic Scholar API
        └── 命中 → 提取元数据比对 → 通过/标记差异
              └── 未命中 → 渠道 3（WebSearch 多搜索词并行）
                    ├── 并行搜索 6 条搜索词
                    └── 命中 → 提取元数据比对 → 通过/标记差异
                          └── 未命中 → 渠道 4（CNKI DOI 结构分析）/渠道 5（人工核验）
```

---

### 渠道 1：DOI 解析（含 DOI 文献优先使用）

```
第一层：doi.org CSL JSON API（国际 DOI，成功率最高）
  curl -sL -H "Accept: application/vnd.citationstyles.csl+json" "https://doi.org/{DOI}"
  → 适用于 CrossRef 注册的国际 DOI（10.1111/、10.1002/、10.1016/、10.1097/ 等）

第二层（Cloudflare 防护的 DOI 降级方案）：
  CrossRef API：
    curl -sL -H "User-Agent: Mozilla/5.0 (compatible; AcademicBot/1.0)" "https://api.crossref.org/works/{DOI}"
  PubMed E-utilities API：
    curl -s "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term={DOI}[DOI]&retmode=json"
  → 当 doi.org 返回 Cloudflare 拦截页面时使用
  → 适用于 JMIR、PeerJ、Medicine(Baltimore)、LWW 等期刊
```

**CNKI/ISTIC 注册的 DOI（10.3969/、10.16821/、10.3760/、10.3761/、10.16460/、10.3870/、10.14055/、10.11655/ 等前缀）不参与国际 CrossRef/doi.org 基础设施，渠道 1 无法解析，直接跳至渠道 2-5。**

---

### 渠道 2：学术数据库标题检索（不论有无 DOI，API 自动化优先）

部分中文期刊论文虽被 PubMed 等国际数据库收录，但 DOI 不参与 CrossRef 基础设施。此时可通过标题检索在以下数据库中定位：

#### 2a. PubMed E-utilities 标题检索

```
# 第一步：用标题关键词 + 作者搜索
curl -s "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term={标题关键词}[Title]+AND+{第一作者}[Author]&retmode=json&retmax=5"

# 第二步：获取完整元数据（作者、刊名、卷期页码、DOI）
curl -s "https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id={PMID}&retmode=json"
```

**适用**：中华医学会系列期刊（10.3760）、部分中文护理期刊在 PubMed 有收录的论文。

#### 2b. OpenAlex API（免费，无需认证，中文覆盖面持续增长）

```
curl -s "https://api.openalex.org/works?search={标题关键词}&filter=publication_year:{年份}&per_page=5"
```

从返回结果提取：`title`、`authorships`（作者列表）、`primary_location.source.display_name`（刊名）、`doi`、`publication_date`。

#### 2c. Semantic Scholar API（免费，补充覆盖面）

```
curl -s "https://api.semanticscholar.org/graph/v1/paper/search?query={标题关键词}&year={年份}&limit=5&fields=title,authors,journal,year,externalIds"
```

---

### 渠道 3：WebSearch 多搜索词并行（兜底策略的核心）

**这是覆盖面最广的渠道——不论中文/英文、有无 DOI、是否被学术数据库收录，搜索引擎几乎总能找到蛛丝马迹。**

**关键原则：多条搜索词并行尝试，而非单条。每条搜索词覆盖不同的索引库和检索入口，任一条命中即可。**

对每条待核验参考文献，按以下顺序并行发起搜索：

| 优先级 | 搜索词模板 | 目标索引/数据库 | 命中后提取 |
|--------|-----------|---------------|-----------|
| 3a | `"{DOI}"` | Google / Bing 全索引 | 论文标题、作者、刊名页面 |
| 3b | `site:xueshu.baidu.com "{中文标题关键词}" {第一作者}` | 百度学术 | 标题、作者、刊名、DOI、卷期页码 |
| 3c | `site:med.wanfangdata.com.cn "{中文标题}"` | 万方医学 | 标题、作者、刊名、DOI |
| 3d | `"{英文标题关键短语}" {年份}` | Google Scholar / 通用索引 | 论文页面（可能含 DOI） |
| 3e | `"{第一作者}" "{刊名}" {年份} {卷} {期}` | 期刊官网 / 通用索引 | 期刊官网目录页 |
| 3f | `"{完整中文标题}"` | 通用索引（Bing / 百度） | 任何提及该论文的页面 |

**搜索结果交叉比对规则：**
```
1. 从搜索结果页面提取：论文标题、第一作者、刊名、年份、卷、期、页码、DOI
2. 将提取结果与稿件参考文献逐字段比对
3. 至少 3 个核心字段一致（作者+标题+刊名）→ 核验通过
4. 字段不一致 → 标记差异详情，进入下一条搜索词或下一渠道
5. 6 条搜索词均无有效结果 → 进入渠道 4/5
```

**百度学术 (xueshu.baidu.com) 特别说明：**
百度学术是中文文献覆盖面最广的免费学术搜索引擎，其索引涵盖 CNKI、万方、维普三大中文数据库，对中文护理学期刊文献的检索成功率远高于 Google Scholar。是渠道 3 中最重要的搜索入口。

---

### 渠道 4：CNKI DOI 结构分析

当渠道 2-3 均无法确认时，对 CNKI/ISTIC DOI 进行结构分析：

```
CNKI DOI 格式：10.XXX/j.cnki.ISSN.YYYY.MM.NNN
               或 10.XXX/j.issn.ISSN.YYYY.MM.NNN

可验证项：
- YYYY：出版年份 → 与稿件中的年份比对
- MM：月份/期号 → 与稿件中的期号比对
- ISSN：期刊 ISSN → 可与期刊 ISSN 比对（间接验证刊名）

红旗信号（DOI 可能抄错）：
- 后缀以 .0 结尾（如 .07.0）→ 可能截断，DOI 不完整
- 后缀序列号异常（如 .0012，正常 CNKI 后缀为 3 位 .012）
- YYYY 与稿件年份差 ≥ 2 年
- MM 与稿件期号不匹配
```

---

### 渠道 5：人工核验（渠道 1-4 均失败时）

| 数据库 | URL | 说明 |
|--------|-----|------|
| 万方医学 | https://med.wanfangdata.com.cn/ | 护理学文献收录较全 |
| 中国知网 | https://wap.cnki.net/ | 移动版界面较简洁 |
| 维普 (CQVIP) | http://www.cqvip.com/ | 第三大中文数据库，部分期刊独家收录 |

**人工核验时注意：**
- 三大数据库均存在反爬机制（验证码/行为分析/IP限流），程序化访问成功率低
- 优先完成渠道 1-4 的自动化核验，仅对自动化全部失败的条目进行人工核验

---

### 新增：无 DOI 文献的核验策略

**无 DOI 不代表无法核验。** 通过渠道 2（学术数据库标题检索）+ 渠道 3（WebSearch 多搜索词并行），可确认文献是否真实存在及元数据是否准确。

```
核验流程：
1. 逐条标记所有无 DOI 的参考文献
2. 优先通过渠道 2（PubMed / OpenAlex 标题检索）核验
3. 渠道 2 失败 → 渠道 3 WebSearch 多搜索词并行（6 条搜索词）
4. 确认文献存在且字段匹配 → ✅ 核验通过，建议补充检索到的 DOI
5. 无法确认文献存在 → ⚠️ 标记"未经核验"，建议作者补充 DOI 或替换
6. 确认文献不存在 → 🔴 标记"文献可能不存在"，建议删除并替换
```

---

### 核验加速技巧

- DOI 以 `10.3760/cma.j.cn` 开头的为中华医学会系列期刊文献 → 渠道 1 无效，直接走渠道 2a（PubMed 标题检索）+ 渠道 3b（百度学术）
- DOI 以 `10.1111/`、`10.1002/` 开头的为 Wiley 期刊（CrossRef 注册）→ 渠道 1 第一层即可核验
- DOI 以 `10.3969/`、`10.16821/` 开头的为 CNKI/ISTIC 注册 DOI → 渠道 1 无效，优先渠道 3b（百度学术）
- 中文文献的英文翻译行 → 可对照中文条目数据核验（无需联网，但需逐条比对卷期页码）
- Cloudflare 防护期刊（JMIR、PeerJ、LWW/Medicine）→ 渠道 1 第二层 CrossRef API 即可绕过
- **CNKI DOI 后缀异常检测**：后缀格式 `.0`（截断）或 `.0012`（异常 4 位序列）为红旗信号，优先走渠道 3
- **无 DOI 的英文文献**：优先 PubMed 标题检索（渠道 2a），命中率高
- **无 DOI 的中文文献**：优先百度学术搜索（渠道 3b），其次万方搜索（渠道 3c）


---

## 三、格式检测正则速查

### 标点错误

| 检测目标 | 正则 | 说明 |
|---------|------|------|
| 中文全角冒号混入参考文献 | `：` | 英文参考文献必须用 `:` |
| 中文全角逗号混入参考文献 | `，` | 英文参考文献必须用 `,` |
| 中文全角句号混入参考文献 | `。` | 英文参考文献必须用 `.` |
| 逗号后缺空格 | `,([A-Z])` | 逗号后应为 `, ` |
| DOI 前缺空格 | `\.DOI:` 或 `\.doi:` | 应为 `. DOI:` |
| DOI 小写 | `doi:` | 应为 `DOI:` |
| 刊名与年份间缺空格 | `[J]\.([A-Z][a-z]+),\d` | 应为 `[J]. 刊名, 年` |
| 期刊名与年份间缺空格 | `[J]\.\w+,\d{4}` | 检查是否有空格 |
| 年份后句点而非逗号 | `\d{4}\.\d+\(` | 应改为 `\d{4}, \d+(` |
| 单词粘连 | `[a-z][a-z]+practice` 等 | 检查常见粘连词 |

### 文献类型标识缺失检测

条目中不包含 `[J]` `[M]` `[D]` `[R]` `[S]` `[EB/OL]` `[C]` `[P]` → 标记

### 卷/期/页码格式错误

| 检测目标 | 正则 | 说明 |
|---------|------|------|
| 缺卷号 | `,\d{4}\(\d+\):` | 年直接连期号，缺少卷号 |
| 缺期号 | `,\d{4},\d+:` | 有卷无期 |
| 页码范围异常 | `:\d+-\d+` | 检查起止页是否正常 |

---

## 四、英文期刊名称对照

以下为护理学领域常见中文期刊及其官方英文名称：

| 中文刊名 | 官方英文名称/缩写 |
|---------|-----------------|
| 中华护理杂志 | Chinese Journal of Nursing / Chin J Nurs |
| 中华现代护理杂志 | Chinese Journal of Modern Nursing / Chin J Mod Nurs |
| 护理学杂志 | Journal of Nursing Science / J Nurs Sci |
| 护理研究 | Chinese Nursing Research |
| 护理学报 | Journal of Nursing (China) / J Nurs |
| 护理管理杂志 | Journal of Nursing Administration / J Nurs Adm |
| 护士进修杂志 | Journal of Nurses Training / J Nurs Train |
| 中国护理管理 | Chinese Nursing Management / Chin Nurs Manag |
| 中华护理教育 | Chinese Journal of Nursing Education / Chin Nurs Educ |
| 上海护理 | Shanghai Nursing |
| 天津护理 | Tianjin Journal of Nursing |
| 护理实践与研究 | Nursing Practice and Research |
| 中华烧伤杂志 / 中华烧伤与创面修复杂志 | Chinese Journal of Burns / Chin J Burns |
| 中国组织工程研究 | Chinese Journal of Tissue Engineering Research |
| 中国卫生统计 | Chinese Journal of Health Statistics |
| 卫生经济研究 | Health Economics Research |
| 中国现代医生 | China Modern Doctor |
| 中国药物与临床 | Chinese Remedies & Clinics |
| 中国当代医药 | China Modern Medicine |
| 中西医结合护理 | Journal of Integrative Nursing / Nursing of Integrated Traditional Chinese and Western Medicine |
| 医学与法学 | Medicine and Law |
| 华西医学 | West China Medical Journal |
| 青岛医药卫生 | Qingdao Medical Journal |

常见错误：
- `Journal of Nursing`（缺 `Science`）→ 应为 `Journal of Nursing Science`
- `Chinese Journal of Nursing` 写为 `China Journal of Nursing`
- 混淆 `Chinese Nursing Research` 和 `Chinese Journal of Nursing`
- `Modern Chinese doctors` → 应为 `China Modern Doctor`
- `Journal of Clinical Nursing in Practice` → 应为 `Journal of Integrative Nursing`（中西医结合护理）
- `Chinese Journal of Burns` vs `Chinese Journal of Burns and Wound Repair`（期刊更名，需按出版年确认）

---

## 五、中文作者拼音规范

### 标准规则（GB/T 28039-2011《中国人名汉语拼音字母拼写规则》）

- 姓在前，名在后，姓和名分写
- 姓全大写或仅首字母大写（学术期刊通常首字母大写）
- 名连写，首字母大写
- 双名中间不加连字符

**示例：**
| 中文名 | 正确拼音 | 常见错误 |
|--------|---------|---------|
| 魏力 | Wei Li | Wei L（缺名字全拼） |
| 张京慧 | Zhang Jinghui | Zhang JH（缩写不完整）/ Jinghui Z（姓在名后） |
| 王晓明 | Wang Xiaoming | Wang XM / Xiaoming Wang |
| 欧阳志远 | Ouyang Zhiyuan | Ou Yang Z Y（复姓被拆分） |

### 英文缩写格式

GB/T 7714-2015 规定英文作者采用"姓全称 名首字母"格式：
- `Wang XM`（名双字各取首字母，无空格无连字符）
- 全文缩写格式保持一致（统一用 `Wang XM` 或 `Wang X.M.`，不混用）

---

## 六、常见文献类型标识速查

| 标识 | 类型 | 示例 |
|------|------|------|
| [J] | 期刊论文 | 护理研究, 2024, 39(1):1-10. |
| [M] | 专著/书籍 | 魏力. 伤口护理实践快速成长手册[M]. ... |
| [D] | 学位论文 | 耿婕. 不同敷料预防压力性损伤的网状Meta分析... [D]. 兰州大学, 2023. |
| [R] | 报告 | WHO. Global status report... [R]. Geneva: WHO, 2022. |
| [S] | 标准 | 甘肃省市场监督管理局. 慢性伤口护理技术规程... [S]. |
| [EB/OL] | 电子资源 | 国家卫生健康委办公厅. ... [EB/OL]. (2020-12-08)[2025-05-27]. https://... |
| [C] | 会议论文集 | |
| [P] | 专利 | |

---

## 七、英文标题自译检测

### 问题本质

中文期刊论文的英文翻译行中，英文标题应使用期刊官网/DOI 注册时登记的标准英文标题（官方标题），而非作者自行翻译。**自译标题导致国际数据库检索无法命中，等同于文献引用失效。**

### 红旗信号

| 信号 | 说明 | 示例 |
|------|------|------|
| 术语与学术惯例不符 | 核心术语翻译错误 | `stress injury` → `pressure injury` |
| 刊名为自译而非官方名 | 刊名完全错误 | `Modern Chinese doctors` → `China Modern Doctor` |
| 标题语法生硬 | 逐字直译、Chinglish | `Applied research on the intervention strategy of secondary healing of chronic wound biofilm in elderly patients` |
| 英文标题完全缺失 | 中文条目有英文翻译行但缺英文标题 | 英文行只有作者+刊名，无标题 |
| 刊名缺词/多词 | 与官方刊名有差异 | `Journal of Nursing` 缺 `Science` |

### 检测流程

```
1. 对每条含中文条目的英文翻译行，提取英文标题和英文刊名
2. 通过 WebSearch 搜索"{中文标题关键词} {英文刊名}"，
   从期刊官网/PubMed/万方 获取该论文的官方英文标题
3. 对比稿件英文标题与官方英文标题：
   - 完全一致 → ✅ 官方标题
   - 仅标点/大小写差异 → 🟡 格式变异
   - 用词不同（术语、语序、刊名） → 🔴 自译标题
   - 稿件无英文标题但期刊官网有 → 🟡 遗漏
4. 对英文刊名，对照本手册"四、英文期刊名称对照"进行核验
```

### 护理学稿件英文术语速查

以下为护理学压力性损伤/互联网+护理领域的高频术语对照，用于检测英文翻译行中的术语错误：

| 中文术语 | 正确英文 | 常见错误翻译 |
|---------|---------|-------------|
| 压力性损伤 | pressure injury | stress injury / pressure ulcer（过时术语）/ pressure sore |
| 失能老人 | disabled elderly / elderly with disabilities | disabled old people / incapacitated elderly |
| 互联网+护理服务 | Internet Plus nursing service | Internet and nursing / online nursing / web-based nursing |
| 循证护理 | evidence-based nursing | evidence nursing |
| 系统评价 | systematic review | systematic evaluation |
| Meta 分析 | meta-analysis | Meta analysis（缺连字符）|
| 网状 Meta 分析 | network meta-analysis | mesh meta-analysis / reticulated meta-analysis |
| 德尔菲法 | Delphi method | Delphi technique / Delphy method |
| 专家共识 | expert consensus | expert agreement / specialist consensus |
| 质性研究 | qualitative study / qualitative research | qualitative analysis / nature research |
| 伤口造口失禁 | wound, ostomy, and continence | wound stoma incontinence |
| 信效度 | reliability and validity | reliability and effectiveness |
| 延续护理 | transitional care / continuous nursing | continuing nursing / extended care |
| 伤口床准备 | wound bed preparation | wound bed ready / wound surface preparation |
| 湿性愈合 | moist wound healing | wet healing / moisture healing |
| 创面修复 | wound repair / wound healing | wound repairation / trauma repair |

### 自译标题与官方标题对比示例

以下为真实审读中发现的自译标题案例：

```
[60] 中文：张乐乐,战青,宋旭林,等. 重组人表皮生长因子治疗压力性损伤疗效的系统评价[J].

       自译英文标题：Systematic review of the efficacy of recombinant human epidermal
                      growth factor in the treatment of stress injury

       官方英文标题：Efficacy of recombinant human epidermal growth factor in the
                     treatment of pressure injury: a systematic review

       错误点：① "stress injury" → "pressure injury"（术语错误）
              ② 标题结构不符合英文论文标题惯例

[67] 中文：朱月兰,汪亚男,徐霞艳. "互联网+护理服务"质量评价指标研究范围综述[J].

       自译刊名：Modern Chinese doctors
       官方刊名：China Modern Doctor
```
