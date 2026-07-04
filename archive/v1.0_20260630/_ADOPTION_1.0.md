# 第三方项目采用指南 / Third-Party Project Adoption Guide

本文档为企业、团队或个人采用 QNLOO-SPL 主权公开许可范式提供标准化操作指引，涵盖模板获取、信息替换、双许可配置、标注规范与修改边界说明。

This document provides standardized operational guidance for enterprises, teams, or individuals adopting the QNLOO-SPL Sovereign Public License Paradigm, covering template acquisition, information replacement, dual-license configuration, labeling specifications, and modification boundary instructions.

---

## 1. 适用范围与前置说明 / Scope & Prerequisites

本指南适用于所有希望将自身数字资产项目纳入 QNLOO-SPL 范式体系的第三方主体。采用本范式为完全自愿行为，一旦在项目中使用 QNLOO-SPL 许可文件并标注范式身份，即视为认可并接受本范式的核心框架与通用规则。

This guide applies to all third-party entities wishing to include their digital asset projects under the QNLOO-SPL paradigm system. Adoption of this paradigm is entirely voluntary. Once the QNLOO-SPL license file is used in a project and the paradigm identity is labeled, it is deemed recognition and acceptance of the core framework and general rules of this paradigm.

采用方须理解并认同 QNLOO-SPL 的基础架构：**计算机源代码适用 Apache License 2.0 宽松开源协议；协议文本、白皮书、专利文书、音频作品、体系逻辑及商业运营行为适用 QNLOO-SPL 主权商事许可**。二者边界清晰、协同生效，共同构成完整的项目授权体系。

Adopters shall understand and acknowledge the basic architecture of QNLOO-SPL: **Computer source code is subject to the permissive Apache License 2.0; protocol text, whitepapers, patent documents, audio works, system logic, and commercial operations are subject to the QNLOO-SPL sovereign commercial license**. The two have clear boundaries and take effect collaboratively, together forming a complete project authorization system.

---

## 2. 分步采用流程 / Step-by-Step Adoption Process

### 步骤 1：获取官方模板 / Step 1: Obtain the Official Template

从 QNLOO-SPL 官方基准仓库的 `template/` 目录下载完整复用模板包，包含主许可文件、Apache 协议文件、专利声明模板及配套说明文档。

Download the complete reuse template package from the `template/` directory of the official QNLOO-SPL reference repository, including the main license file, Apache license file, patent declaration template, and supporting documentation.

### 步骤 2：替换基础主体信息 / Step 2: Replace Basic Entity Information

将模板中所有占位符替换为项目自身信息，可替换项包括：
- 资产持有主体全称（中英文）
- 项目官方网站或溯源地址
- 项目专属的营收阈值、授权费率等商业参数
- 自有专利清单与专利局信息

Replace all placeholders in the template with the project's own information. Replaceable items include:
- Full name of the asset holding entity (Chinese and English)
- Official project website or traceability address
- Commercial parameters such as project-specific revenue thresholds and authorization rates
- Own patent list and patent office information

### 步骤 3：配置仓库许可文件 / Step 3: Configure Repository License Files

将以下文件放置于项目仓库根目录，保持命名规范与官方基准仓库一致：

- `LICENSE`：放置项目**引导型多重许可声明**（固定路由文件，禁止放置任何开源协议正文）。前置声明双资产分离架构，强制引导自动化合规扫描工具进行人工审计。
- `LICENSE-APACHE`：放置 Apache License 2.0 全文（固定文件，专门对应源代码类资产）
- `LICENSE-QNLOO-SPL`：放置 QNLOO-SPL 主权公开许可范式全文（固定文件，专门对应创作资产与商业运营）
- `PATENTS`：放置项目专利授权说明书（固定文件，专门对应专利授权）
- **【纯商业闭源项目特别通道】**：若采用方项目属于商业闭源形态（底层源代码不向任何第三方公开，仅公开白皮书、API 架构或商用协议），**须在根目录中彻底删除 `LICENSE-APACHE` 文件**，并在主 `LICENSE` 路由文件中将源码声明修改为“【计算机源代码类资产】：完全闭源专有，不授予任何开源许可”。


Place the following files in the root directory of the project repository, keeping the naming conventions consistent with the official reference repository:

- `LICENSE`: Contains the project's **Guided Multi-License Notice** (a fixed routing file; standard license prose MUST NOT be placed here). It explicitly declares the dual-asset separation framework to guide automated compliance scanners toward manual legal audits.
- `LICENSE-APACHE`: Contains the full text of the Apache License 2.0 (fixed file, dedicated to source code assets)
- `LICENSE-QNLOO-SPL`: Contains the full text of the QNLOO-SPL Sovereign Public License Paradigm (fixed file, dedicated to creative assets and commercial operations)
- `PATENTS`: Contains the project patent grant addendum (fixed file, dedicated to patent grants)
- **[Proprietary Closed-Source Passage]**: If the adopting project is entirely proprietary and closed-source (source code is strictly confidential and not public, only whitepapers or APIs are disclosed), the `LICENSE-APACHE` file **MUST be completely removed from the repository**, and the master `LICENSE` routing file must state: "[Computer Source Code Assets]: Strictly proprietary and closed-source; no open-source license granted."

> 补充说明：若项目无专利资产，`PATENTS` 文件仍应保留，并替换为无专利占位声明；若项目仅包含源代码类资产（无文本、专利、音频等创作资产），`LICENSE-QNLOO-SPL` 和 `PATENTS` 可省略，仅保留 `LICENSE`（Apache 2.0）和 `LICENSE-APACHE`。

> Supplementary Note: If the project has no patent assets, the `PATENTS` file should still be retained and replaced with the no-patent placeholder statement. If the project contains only source code assets (no creative assets such as text, patents, or audio), the `LICENSE-QNLOO-SPL` and `PATENTS` files may be omitted, retaining only `LICENSE` (Apache 2.0) and `LICENSE-APACHE`.

### 步骤 4：完善专利授权声明 / Step 4: Complete the Patent Grant Declaration

若项目包含已提交的专利，在 `PATENTS` 文件中填写完整专利清单；若暂无已提交专利，删除专利表格并保留无专利占位声明即可。

If the project includes filed patents, fill in the complete patent list in the `PATENTS` file. If no patents have been filed yet, delete the patent table and retain the no-patent placeholder statement.

### 步骤 5：添加项目首页标注 / Step 5: Add Project Homepage Labeling

在项目 README 首页的许可声明区域，添加标准范式标注话术（见本文第 4 节），并链接至 QNLOO-SPL 官方基准仓库。

Add the standard paradigm labeling statement (see Section 4 of this document) in the license declaration area of the project's README homepage, and link to the official QNLOO-SPL reference repository.

### 步骤 6：合规性自检 / Step 6: Compliance Self-Check

发布前确认：核心法律条款未私自删减、双许可边界描述准确、营收与计费规则清晰、标注话术规范。

Before release, confirm that: core legal clauses have not been privately deleted, dual-license boundary descriptions are accurate, revenue and billing rules are clear, and labeling statements are standardized.

---

## 3. 可修改范围与禁止边界 / Modification Scope & Restrictions

### 3.1 允许自定义的内容 / 3.1 Permitted Customizations

在保持范式核心框架不变的前提下，采用方可对以下内容进行自定义调整：
1. 资产持有主体的名称、地址、官网等身份信息；
2. 分级授权的营收阈值、授权费率等商业参数；
3. 自有专利的清单、编号与保护范围；
4. 过渡期的时长与具体结算规则；
5. 项目自身的补充说明与操作指引。

Under the premise of keeping the core framework of the paradigm unchanged, adopters may customize the following content:
1. Identity information such as the name, address, and official website of the asset holding entity;
2. Commercial parameters such as revenue thresholds and authorization rates for tiered authorization;
3. List, numbers, and protection scope of own patents;
4. Duration of the transition period and specific settlement rules;
5. Supplementary descriptions and operational guidelines for the project itself.

### 3.2 禁止修改的核心条款 / 3.2 Prohibited Modifications to Core Clauses

为保障 QNLOO-SPL 范式的统一性与法律严谨性，以下核心条款不得私自删减、篡改或实质性变更：
1. 双资产分层许可隔离的基础架构定义；
2. 主权法定数字货币结算的核心机制定位（采用方须锚定发行主体所在主权国家的法定数字货币作为基准结算通道；任何实质性偏离本定位、以非主权代币或私人虚拟积分替代法定基准结算通道的修改，视为对核心条款的实质性变更）；
3. 梯度化清算违约金的公允补偿定性与分层逻辑；
4. 跨法域司法适配的通用转化规则；
5. 属地冲突分割生效的法律保全条款；
6. 分布式吹哨人维权的基础收益分成机制。


To ensure the uniformity and legal rigor of the QNLOO-SPL paradigm, the following core clauses shall not be privately deleted, tampered with, or substantially changed:
1. Basic architecture definition of dual-asset tiered licensing isolation;
2. Core mechanism positioning of sovereign statutory digital currency settlement (Adopters shall anchor the statutory digital currency of the sovereign state where the issuing entity is located as the benchmark settlement channel; any modification that substantively deviates from this positioning by substituting the legal benchmark settlement channel with non-sovereign tokens or private virtual points shall be deemed a substantive change to core clauses);
3. Fair compensation definition and tiered logic of gradient liquidated damages;
4. General conversion rules for cross-jurisdictional judicial adaptation;
5. Legal preservation clauses for severability in case of local law conflicts;
6. Basic revenue sharing mechanism for distributed Qui Tam enforcement.

对核心条款进行实质性修改的项目，不再属于 QNLOO-SPL 范式体系，不得使用“QNLOO-SPL 范式”相关标识进行对外宣传。

Projects that make substantive modifications to core clauses shall no longer belong to the QNLOO-SPL paradigm system and may not use "QNLOO-SPL Paradigm" related identifiers for external publicity.

---

## 4. 标准标注与命名规范 / Standard Labeling & Naming Rules

### 4.1 README 标准标注话术 / 4.1 Standard README Labeling Statement

推荐在项目 README 顶部许可说明处使用以下统一表述：

The following unified statement is recommended for use in the license description at the top of the project README:

> 本项目数字创作资产、商用运营行为采用 **QNLOO-SPL 主权公开许可范式**；计算机源代码单独遵循 Apache License 2.0。
 
> The digital creative assets and commercial operations of this project adopt the **QNLOO-SPL Sovereign Public License Paradigm**; computer source code is separately governed by the Apache License 2.0.

### 4.2 仓库文件命名规范 / 4.2 Repository File Naming Rules

为保持范式体系的识别一致性，推荐采用以下命名规则：
- 主许可文件：`LICENSE`（根目录，便于平台自动识别）
- 源码开源协议：`LICENSE-APACHE`
- 专利声明文件：`PATENTS`
- 范式采用指南：`ADOPTION.md`

To maintain identification consistency across the paradigm system, the following naming rules are recommended:
- Main license file: `LICENSE` (root directory, for automatic platform recognition)
- Source code open-source license: `LICENSE-APACHE`
- Patent declaration file: `PATENTS`
- Paradigm adoption guide: `ADOPTION.md`

---

## 5. 常见问题 / Frequently Asked Questions

### Q1：没有已提交的专利，可以采用本范式吗？/ Can this paradigm be adopted without filed patents?

可以。QNLOO-SPL 范式不强制要求项目持有专利，无专利项目可直接使用无专利占位声明，仅对文本、音乐等创作资产及商业运营行为进行授权约束。

Yes. The QNLOO-SPL paradigm does not mandate that projects hold patents. Projects without patents may directly use the no-patent placeholder statement, and only impose authorization constraints on creative assets such as text and music, as well as commercial operations.

### Q2：可以调整授权费率和营收阈值吗？/ Can the authorization fee rates and revenue thresholds be adjusted?

可以。采用方可根据自身项目定位自定义费率与阈值，但须保持分层授权的基础结构，且调整后的参数须在许可文件中清晰公示。

Yes. Adopters may customize rates and thresholds according to their own project positioning, but must maintain the basic structure of tiered authorization, and the adjusted parameters must be clearly disclosed in the license file.

### Q3：采用本范式需要向官方报备或付费吗？/ Does adopting this paradigm require reporting to or paying the official?

不需要。QNLOO-SPL 范式面向全行业开放复用，无需申请、无需付费、无需报备，按本指南规范配置并标注即可。范式官方不参与第三方项目的商业运营与收益分配。

No. The QNLOO-SPL paradigm is open for industry-wide reuse. No application, no fee, and no reporting are required. Simply configure and label in accordance with this guide. The paradigm official does not participate in the commercial operation or revenue distribution of third-party projects.

### Q4：闭源商业项目可以采用本范式吗？ / Can proprietary commercial projects adopt this paradigm?

可以。本范式不强制项目开源全部代码，仅要求源代码部分遵循 Apache 2.0 规则，商业运营与创作资产部分遵循 QNLOO-SPL 规则，适用于开源、源码可用及商业闭源等多种项目形态。

Yes. This paradigm does not mandate that projects open-source all code. It only requires that the source code part follows Apache 2.0 rules, and commercial operations and creative assets follow QNLOO-SPL rules. It is applicable to various project forms such as open-source, source-available, and commercial proprietary projects.

---

**© 2026 千年鹿 QNLOO**

**厦门千年鹿文化科技有限公司 / Xiamen QNLOO Culture & Technology Co., Ltd.**

**文档版本 / Document Version**: v1.1

**生效日期 / Effective Date**: 2026年6月30日

**版本修订日期 / Version Revision Date**: 2026年7月4日