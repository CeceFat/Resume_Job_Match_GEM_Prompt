# Resume–Job Match Analyst | 履歷–職缺匹配分析器

**A structured LLM prompt for evidence-based resume screening, inspired by patent claim analysis methodology.**

**一套結構化的 LLM 提示詞，用於 evidence-based 的履歷篩選，靈感來自專利請求項分析方法論。**

---

## What is this? | 這是什麼？

This is a system prompt (designed for Google AI Studio GEMs, but compatible with any LLM that supports system instructions) that transforms an AI into a rigorous **Resume–Job Description matching analyst**.

這是一個系統提示詞（設計用於 Google AI Studio GEMs，但相容於任何支援 system instruction 的 LLM），可將 AI 轉化為嚴謹的**履歷–職缺比對分析師**。

Instead of vague keyword matching, it applies a **claim construction methodology** — originally developed for Standard Essential Patent (SEP) essentiality analysis — to decompose job requirements element-by-element and map them against resume evidence with strict evidentiary standards.

它不採用模糊的關鍵字比對，而是應用**請求項解構方法論** —— 原始開發於標準必要專利（SEP）essentiality 分析 —— 將職缺需求逐項拆解，並以嚴格的佐證標準比對履歷內容。

---

## Origin Story | 起源

As a patent engineer, I built a cognitive architecture for SEP essentiality checks — a workflow that deconstructs patent claims element-by-element, maps each against a technical standard, and produces a structured verdict with dialectical analysis.

身為專利工程師，我為 SEP essentiality check 建構了一套認知架構 —— 一個將專利請求項逐 element 拆解、逐項比對技術標準、並產出結構化結論與辯證分析的工作流程。

I realized the **structural isomorphism** between these two tasks:

我發現這兩項任務之間存在**結構同構性**：

| SEP Essentiality Check | Resume–JD Matching |
|---|---|
| Patent claim → element decomposition | Job description → requirement decomposition |
| Standard text → normative evidence | Resume → experience evidence |
| MAPPED / PARTIAL / NOT_FOUND | STRONG MATCH / PARTIAL MATCH / GAP |
| Essentiality score | Match score |
| Thesis–Antithesis–Synthesis | Thesis–Antithesis–Synthesis |
| Cui Bono? (licensing strategy) | Cui Bono? (hiring strategy) |

So I ported the methodology. This is the result.

因此我移植了這套方法論。這就是成果。

---

## Key Features | 核心特色

### 1. Element-by-Element Decomposition | 逐項拆解
JD requirements are decomposed into discrete, categorized elements (Hard Skill, Soft Skill, Domain Knowledge, Credential, Experience, Logistics), each assigned a weight (MUST-HAVE / NICE-TO-HAVE / IMPLICIT).

JD 需求被拆解為離散的、分類過的元素（硬技能、軟技能、領域知識、證照、經歷、後勤條件），每項賦予權重（必備 / 加分 / 隱性）。

### 2. Strict Evidence Standards | 嚴格佐證標準
Four-tier matching: **STRONG MATCH** (concrete evidence + quantified outcomes) → **PARTIAL MATCH** (related but incomplete) → **INFERRED** (reasonable inference, needs verification) → **GAP** (not found). No "vibes-based" assessment.

四級匹配制：**STRONG MATCH**（具體證據 + 量化成果）→ **PARTIAL MATCH**（相關但不完整）→ **INFERRED**（合理推論，需驗證）→ **GAP**（未找到）。不做「感覺式」評估。

### 3. Four Corners Rule | 四角原則
Analysis is grounded in the actual text of the resume and JD — not assumptions, brand halo, or gut feeling. Domain knowledge serves as reference, never as substitute for evidence.

分析基於履歷與 JD 的實際文字 —— 而非假設、品牌光環或直覺。領域知識僅作參考，絕不替代證據。

### 4. Dialectical Analysis | 辯證分析
Every conclusion undergoes Thesis (direct analysis) → Antithesis (candidate's defense, hiring manager's concerns, market dynamics) → Synthesis (pragmatic verdict + confidence interval + known unknowns).

每個結論都經過正題（直接分析）→ 反題（候選人辯護、用人主管顧慮、市場供需）→ 合題（務實結論 + 信心區間 + 已知未知）。

### 5. Transferable Skills Analysis | 可遷移能力分析
Distinguishes between direct transfer, proximate transfer (same category, short learning curve), conceptual transfer (same underlying logic), and weak transfer — preventing both over-crediting and under-crediting cross-domain experience.

區分直接遷移、近似遷移（同類技能，短學習曲線）、概念遷移（底層邏輯相同）與弱遷移 —— 避免對跨域經歷過度或不足地評價。

### 6. Anti-Bias Compliance Reminders | 反歧視合規提醒
Built-in detection for discriminatory JD clauses and explicit prohibition against age, gender, race, or other protected-class-based assessments.

內建歧視性 JD 條款偵測，明確禁止基於年齡、性別、種族等受保護類別的評估。

---

## How to Use | 使用方式

### Google AI Studio (GEMs)
1. Go to [Google AI Studio](https://aistudio.google.com)
2. Create a new GEM
3. Paste the entire content of `Resume_Job_Match_GEM_Prompt.md` into the **System Instruction** field
4. Start a conversation by providing a JD and a resume

### Other LLM Platforms | 其他 LLM 平台
Paste the prompt content into the system prompt / system instruction field of any compatible platform (Claude, ChatGPT custom instructions, etc.).

將提示詞內容貼入任何相容平台的 system prompt / system instruction 欄位（Claude、ChatGPT 自訂指示等）。

---

## Output Structure | 輸出結構

The prompt produces a structured report containing:

提示詞產出結構化報告，包含：

1. **Executive Summary** — Bottom-line verdict (STRONG FIT / GOOD FIT / PARTIAL FIT / WEAK FIT) with confidence level
2. **Matching Chart** — Element-by-element mapping table with evidence citations
3. **Gap Analysis** — Critical gaps, manageable gaps, and hidden strengths
4. **Dialectical Analysis** — Thesis / Antithesis / Synthesis
5. **Strategic Recommendation** — Cui Bono analysis, interview verification checklist, JD revision suggestions, or career advice (depending on use case)

---

## Limitations & Disclaimer | 限制與免責聲明

⚠️ **This tool does not constitute employment advice, legal advice, or hiring decisions.**

⚠️ **本工具不構成僱用建議、法律意見或錄用決策。**

- LLM outputs are probabilistic and may contain errors. All matching results should be verified by qualified HR professionals or hiring managers.
- The compliance reminders (anti-discrimination, labor law) are informational prompts, **not legal opinions**. Consult qualified legal counsel for compliance questions.
- **Privacy notice**: Inputting resumes into any LLM involves processing personal data. Users are responsible for complying with applicable data protection regulations (GDPR, Taiwan PDPA, etc.) and reviewing the data usage policies of their chosen LLM platform.
- The scoring formula is a heuristic framework, not a validated psychometric instrument.

- LLM 輸出為機率性結果，可能包含錯誤。所有匹配結果應由合格的人資專業人員或用人主管驗證。
- 合規提醒（反歧視、勞動法規）為資訊性提示，**非法律意見**。合規問題請諮詢合格法律顧問。
- **隱私注意事項**：將履歷輸入任何 LLM 涉及個人資料處理。使用者有責任遵守適用的資料保護法規（GDPR、臺灣個資法等），並審閱所選 LLM 平台的資料使用政策。
- 評分公式為啟發式框架，並非經過驗證的心理測量工具。

---

## Methodology Cross-Reference | 方法論對照

For those interested in the original patent analysis methodology that inspired this project:

對原始專利分析方法論有興趣者：

| Concept | In SEP Analysis | In Resume Matching |
|---|---|---|
| **Decomposition unit** | Claim element | JD requirement |
| **Evidence source** | Technical standard text | Resume content |
| **Construction standard** | Phillips v. AWH Corp. (2005) | POSITA → Hiring manager perspective |
| **Mapping strictness** | MAPPED requires specific section + page + quote | STRONG MATCH requires specific experience + timeline + outcome |
| **Cross-layer problem** | Standard defines mechanism ≠ standard mandates specific usage | Resume shows exposure ≠ resume proves ownership |
| **Scoring threshold** | 100% MAPPED = ESSENTIAL | ≥85% weighted = STRONG FIT |

---

## Language | 語言

The prompt is written in **Traditional Chinese (Taiwan)** with technical terms in English. This reflects its origin as a working tool for the Taiwan talent market. Community contributions for localized versions are welcome.

提示詞以**繁體中文（臺灣）**撰寫，技術術語維持英文。這反映其作為臺灣人才市場工作工具的原始用途。歡迎社群貢獻在地化版本。

---

## Contributing | 貢獻

This prompt was created by a patent engineer, not an HR professional. Contributions from HR practitioners, recruiters, organizational psychologists, and labor law specialists are especially welcome. Areas for improvement include:

此提示詞由專利工程師撰寫，而非人資專業人士。特別歡迎人資從業者、招募人員、組織心理學家與勞動法專家的貢獻。改進方向包括：

- Industry-specific domain knowledge modules (§6) for non-tech sectors
- Validated competency frameworks to replace or supplement the heuristic scoring
- Localization for other markets (US, EU, Japan, Southeast Asia)
- Integration with ATS (Applicant Tracking System) workflows
- Bias detection improvements

---

## License | 授權

[MIT License](LICENSE)

---

## Author | 作者

**CamusTsai**

An IP professional with 15+ years of experience spanning patent litigation (US jurisdiction), SEP/FRAND licensing negotiations, and cross-functional IP risk management in the semiconductor and telecommunications industries. Day-to-day work involves deconstructing patent claims against technical standards — the exact methodology that powers this project.

一位擁有 15 年以上經驗的智慧財產權專業人士，工作橫跨專利訴訟（美國管轄權）、SEP/FRAND 授權談判，以及半導體與通訊產業的跨部門 IP 風險管理。日常工作就是將專利請求項與技術標準進行解構比對 —— 正是驅動本專案的方法論本身。

Having pioneered a "Human-in-the-Loop" framework for integrating generative AI into legal analysis workflows — including adversarial validation protocols to mitigate hallucination risks — the author recognized that the structured rigor of claim construction and essentiality checking could be abstracted and applied to other domain-matching problems. Resume screening, with its need to decompose requirements, weigh evidence, and produce defensible verdicts, turned out to be a natural fit.

在將生成式 AI 整合進法律分析工作流程的過程中，作者建立了「Human-in-the-Loop」框架 —— 包含用於降低幻覺風險的對抗驗證協議。由此體認到，claim construction 與 essentiality check 的結構化嚴謹性可以抽象化並應用於其他領域比對問題。履歷篩選 —— 同樣需要拆解需求、秤量證據、產出可辯護的結論 —— 成為自然的移植對象。

The cognitive architecture was originally built in Claude Code (Opus 4) for professional SEP analysis, then ported to Google AI Studio GEMs format. This resume matching variant is released as open source because it falls outside the author's core professional domain — and is better served by community refinement from actual HR practitioners.

認知架構最初在 Claude Code（Opus 4）中為專業 SEP 分析工作而建構，後移植至 Google AI Studio GEMs 格式。本履歷匹配版本以開源方式發布，正因為它不在作者的核心專業領域內 —— 交由實際的人資從業者透過社群來精進，才是更好的演化路徑。
