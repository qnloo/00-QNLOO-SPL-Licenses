# 法律条款简要释义 / Legal Clauses Summary

**当前适用版本 / Applicable Version**: QNLOO-SPL v1.1

**生效日期 / Effective Date**: 2026年6月30日

**版本修订日期 / Version Revision Date**: 2026年7月4日

**制定主体 / Issuing Entity**: 厦门千年鹿文化科技有限公司 (Xiamen QNLOO Culture & Technology Co., Ltd.)

---

本文件为 QNLOO-SPL v1.1 核心条款的通俗化白话释义，面向非法律专业背景的开发者、企业运营者与生态使用者，旨在消除理解摩擦，帮助快速界定许可边界。**本文件仅作合规理解参考，不构成正式法律意见，不具备直接诉讼效力。所有权利、义务与清算责任，一律以主许可法律文本（LICENSE-QNLOO-SPL）及相关专利文书的字面释义为准。**

This document provides a plain-language interpretation of the core clauses of QNLOO-SPL v1.1, intended for developers, enterprise operators and general users without a legal background, to help quickly understand the core meaning and boundaries of the license rules. **This document is for reference only, does not constitute legal advice, and has no formal legal effect. All rights and obligations shall be subject to the legal text of the LICENSE-QNLOO-SPL master license and related patent documents.**

---

## 1. 分级授权规则释义 / 1. Interpretation of Tiered Authorization Rules

*对应主许可第一部分：分级授权与豁免规则*

### 1.1 个人非商用永久豁免 / Permanent Exemption for Personal Non-Commercial Use

简单理解：自然人出于学习、研究、个人兴趣使用本体系的代码、文档、音乐，永远免费，不需要登记、不需要付费，也不需要标注来源。

Plain meaning: Natural persons using the code, documents and music of this system for learning, research or personal interest are always free of charge, no registration, no payment, and no source attribution required.

判定标准：不以营利为目的，不用于商业产品或服务中，不向第三方收费提供相关服务。

Judgment standard: Not for profit, not used in commercial products or services, and no fees are charged to third parties for related services.

### 1.2 链上合规小微普惠豁免 / Inclusive Exemption for On-Chain Compliant Small & Micro Entities

简单理解：年营收100万元以内的小微企业，只要接入价值协议链的标准接口、公开标注合规身份，就可以免费商用，不需要支付授权费。

Plain meaning: Small and micro enterprises with annual revenue within RMB 1 million can use it commercially for free as long as they access the standard interface of the Value Protocol Chain and publicly label their compliance status, no authorization fee required.

核心要求：必须完成合规并网，业务数据可溯源；营收仅计算相关业务线，不是企业总营收。

Core requirement: Compliance integration must be completed, business data is traceable; revenue only counts for relevant business lines, not the enterprise's total revenue.

### 1.3 累进商业授权 / Progressive Commercial Authorization

简单理解：合规企业年营收超过100万的部分，按0.6%的比例支付授权费，相当于“赚得多才多付”，门槛低、负担轻。
Plain meaning: For compliant enterprises with annual revenue exceeding RMB 1 million, a 0.6% authorization fee is charged on the excess portion — equivalent to "pay more only when you earn more", with a low threshold and light burden.

计费基数：仅针对使用本体系的业务线营收，不是企业全部营收；以公开财报或税务申报数据为准。

Billing base: Only for the revenue of business lines using this system, not the enterprise's total revenue; subject to public financial statements or tax filing data.

### 1.4 外部游离主体计费 / Off-Chain Non-Compliant Charges

简单理解：商用但不接入合规体系、不标注身份的主体，不再享受 100 万免费额度，计费标准自动调整为按全主体合并报表口径下总年营收的 0.6% 持续核算。

Plain meaning: Commercial entities that conduct operations without completing ecological compliance integration lose the RMB 1,000,000 exemption, and their fee calculation standard shall be automatically adjusted to 0.6% of their total annual revenue, calculated continuously based on the consolidated financial statements of the entire entity.

设计目的：鼓励合规并网，通过差异化计费引导商业主体进入透明、可追溯的生态体系。

Design purpose: Encourage compliance integration, and guide commercial entities into a transparent and traceable ecosystem through differentiated billing.

### 1.5 大厂产品线穿透 / Large Enterprise Product Line Revenue Penetration

简单理解：如果单条产品线年营收超过10亿元，且核心功能深度依赖本体系技术逻辑，直接按该产品线全年总流水的0.6%计费，不再享受小微豁免。

Plain meaning: If a single product line generates annual revenue exceeding RMB 1 billion, and its core functions deeply rely on the technical logic of this system, it is directly billed at 0.6% of the product line's full annual revenue, without the small-scale exemption.

### 1.6 法定结算通道 / Statutory Settlement Channel

简单理解：所有授权费、违约金的官方结算渠道是数字人民币智能合约。境外企业有三年过渡期，过渡期内正常授权费可以用跨境对公支付；但因主观恶意逃逸产生的清算违约金，0 缓冲，必须无条件走数字人民币智能合约完成结算。

Plain meaning: The sole legally binding benchmark settlement channel for all funds shall be the e-CNY smart contract. Offshore compliant entities enjoy a 3-year global transition period for regular fees via corporate cross-border channels; however, liquidated damages arising from subjective bad-faith evasion have zero buffer and must unconditionally and exclusively be settled via e-CNY smart contracts, and the cross-border corporate payment buffer shall not apply.

特别说明：恶意侵权产生的违约金，过渡期内也必须走数字人民币结算，不享受缓冲。

Special note: Liquidated damages from malicious infringement must be settled via e-CNY even during the transition period, no buffer applies.

---

## 2. 分布式执法机制释义 / Interpretation of Distributed Enforcement Mechanisms

*对应主许可第二部分：分布式执法与吹哨人机制*

### 2.1 跨法域属地适配  / Cross-Jurisdictional Territorial Adaptation

简单理解：这套规则在不同国家会自动适配当地法律：美国用等同原则和约定损害赔偿规则，欧盟对齐GDPR数据规则，大陆法系国家自动转化为符合当地要求的维权授权。

Plain meaning: This set of rules automatically adapts to local laws in different countries: the US uses the Doctrine of Equivalents and agreed liquidated damages rules; the EU aligns with GDPR data rules; civil law countries automatically convert to enforcement authorization compliant with local requirements.

核心作用：避免“在一个国家有效、在另一个国家无效”的问题，保障全球范围内的可执行性。

Core function: Avoid the problem of "valid in one country, invalid in another", and ensure enforceability worldwide.

### 2.2 分布式社会化取证与司法属地双轨制 / Distributed Standing & Qui Tam Standing Rules

简单理解：为了彻底规避部分大陆法系国家对“事前诉讼信托/代为诉讼”的合规限制，v1.1版本升级为属地双轨制维权：在美国司法辖区内，捕获证据的吹哨人自动取得共同原告资格；在中国大陆、欧盟等全球其余法域，诉讼资格专属资产持有主体或其合法书面授权的律所，吹哨人匿名提供哈希铁证并领取赏金，无需暴露肉身承担法律风险。

Plain meaning: To completely circumvent local legal restrictions on "pre-litigation trusts" or "maintenance" in civil law jurisdictions, the v1.1 framework upgrades to a dual-track enforcement system: within judicial districts of the United States, Qui Tam Relators automatically obtain co-plaintiff standing; in Chinese mainland, the European Union, and all other global jurisdictions, exclusive litigation standing is reserved solely for the asset owner or its lawfully authorized legal counsel in writing, allowing relators to provide evidence anonymously and claim bounties without personal legal exposure.

### 2.3 赏金权利预先让渡机制 / Pre-Assignment of Bounty Rights

简单理解：只要发现有人恶意侵权逃逸，全球任何人均可通过开源“主权取证工具包”捕获特征指纹（如 `0xABCD` 窗口特征字）并向分布式账本存证。所有权人特此作出不可撤销的公开民事处分安排：将侵权赔偿款中超出 0.6% 基准费率的所有溢价收益，全额预先让渡给首位举证成功的吹哨人，作为其维权激励。

Plain meaning: Upon discovering bad-faith infringement, any third party worldwide can utilize the open-source Sovereign Forensic Toolkit to capture fingerprints (including but not limited to the 0xABCD feature flag) and record them on the distributed ledger. The asset owner hereby makes an irrevocable right assignment arrangement: the premium portion of infringement breach compensation exceeding the 0.6% benchmark authorization fee shall be fully and previously assigned to the Qui Tam Relator who successfully provides evidence as their enforcement incentive.

---

## 3. 违约赔偿规则释义 / Interpretation of Default Compensation Rules

*对应主许可第三部分：损害赔偿与合规要求*

### 3.1 赏金分付与权责边界 / Separate Payment of Bounty and Liability Boundaries

简单理解：诉讼或调解成功后，对应 0.6% 年营收的基准费部分作为补缴授权费直接支付给规则制定者；剩余溢价补偿部分，直接分账支付给举证成功的吹哨人作为悬赏激励。所有取证成本、诉讼费、律师费等全部由吹哨人从所得赏金中自行覆盖，规则制定者不承担任何垫付或担保责任。

Plain meaning: Upon successful litigation, mediation, or settlement, the portion corresponding to 0.6% of annual revenue as the benchmark fee shall be paid directly by the infringing entity to the Rule-Maker as overdue system authorization fees; the remaining premium compensation portion shall be paid directly to the successful Qui Tam Relator as an incentive bounty. All enforcement-related expenses, including evidence collection costs and legal fees, shall be borne solely by the relator and covered from the bounty received, and the Rule-Maker assumes no liability or obligation for advance payments.

### 3.2 不真诚违约梯度与1.66倍数学熔断 / Non-Sincere Breach & The 1.66x Model

简单理解：违约侵权按主观程度分为两档：一是无意疏漏，按单年度 0.8% 费率清算，不追加三年连续条款；二是主观恶意逃逸，适用 1.0% 年营收费率，强制连续清算 3 个财务年度。
在恶意的三年清算中，仅首年度的 0.4% 溢价作为悬赏发放给举证极客，后续两年的 0.4% 溢价由规则制定者依法收回，专项转化成长线诉讼博弈的“主权防卫基金”。三年总计赔偿（3%）相比正常合规并网时三年应付的授权费（每年0.6%，三年合计1.8%）仅为 1.66 倍，定性为对全量资产组合受损的合理估算之清算违约金，绝非惩罚性罚金，以排除各主权国法院予以司法裁量酌减之抗辩。

Plain meaning: Breach is categorized into two tiers based on subjective intent: (a) inadvertent omissions, applying a single-year 0.8% rate without the three-year consecutive clause; (b) subjective bad-faith evasion, applying a 1.0% annual revenue fee rate mandatorily and continuously enforced for three fiscal years.
Under the three-year bad-faith liquidation, only the 0.4% premium of the first year constitutes the Qui Tam bounty incentive for the relator; the 0.4% premiums of the subsequent two fiscal years are lawfully reclaimed by the Rule-Maker as additional compensation and dedicated as a standing sovereign defense fund. The total three-year compensation (3%) vs. the normal authorization fees that would have been paid over three years of compliant operation (0.6% annually, 1.8% total) is exactly 1.66x, legally characterized as reasonably estimated liquidated damages for the complete asset portfolio rather than punitive damages, thereby precluding defenses in sovereign courts that seek judicial reduction on the grounds of its punitive nature.

---

### 3.3 公允补偿定性 / Fair Compensation Qualification

简单理解：这些钱不叫“罚款”，叫“清算违约金”，是提前约定好的、对权利人损失的合理补偿，包括声誉损失、维权成本、替代开发成本等。

Plain meaning: These sums are not called "fines", but "liquidated damages" — a pre-agreed reasonable compensation for the rights holder's losses, including reputation damage, enforcement costs, alternative development costs, etc.

法律意义：很多国家的法院会调低“惩罚性罚款”，但会支持“合理预估的违约金”，这样设计是为了让条款在全球法院都更容易被支持。

Legal significance: Courts in many countries will reduce "punitive fines", but will uphold "reasonably estimated liquidated damages". This design makes the clauses more likely to be upheld by courts worldwide.

### 3.4 规则更新与合规要求/ Rule Updates & Compliance Requirements

简单理解：许可规则后续会更新，商业主体有6个月的适配期；到期不更新的，取消免费额度，按全额营收计费。
Plain meaning: License rules will be updated in the future, and commercial entities have a 6-month adaptation period; those who do not update after expiration lose the exemption and are billed on full revenue.

---

## 4. 双许可架构与效力规则释义 / 4. Interpretation of Dual-License Architecture & Effectiveness Rules

### 4.1 双资产分层边界 / Dual-Asset Tiered Boundary

简单理解：代码和内容分开管：

- 源代码：随便用、随便改、随便分发，遵守Apache 2.0就行；
- 白皮书、专利、音乐、商业逻辑、运营规则：受QNLOO-SPL约束，商用要按规则付费。

Plain meaning: Code and content are governed separately:

- Source code: Free to use, modify and distribute, just comply with Apache 2.0;
- Whitepapers, patents, music, business logic, operation rules: Governed by QNLOO-SPL, commercial use requires payment according to rules.

### 4.2 纯商业闭源项目特别通道 / Proprietary Closed-Source Passage

简单理解：本范式完全支持纯商业闭源项目形态。如果项目底层源代码是绝对商业机密，只要从仓库根目录中彻底删除 `LICENSE-APACHE` 文件，并在主 `LICENSE` 路由文件中将源码明确声明为完全闭源专有、不授予任何开源许可，其代码即可继续保持绝对封闭，而上层资产和生态依然完美适配 SPL 的主权保护。

Plain meaning: This paradigm fully supports strictly proprietary closed-source project configurations. If the underlying source code is a core commercial secret, adopters must completely remove the `LICENSE-APACHE` file from the repository and explicitly declare code as "strictly proprietary closed-source; no open-source license granted" in the master `LICENSE` routing file, keeping the core code perfectly locked while the upper-layer assets and ecosystem remain under SPL sovereign protection.

### 4.3 属地分割生效 / Jurisdictional Severability

简单理解：如果某一条规则在某个国家违反当地强制法律，那这一条只在这个国家无效，其他所有条款仍然有效，不会因为一条有问题导致整个许可作废。

Plain meaning: If a clause violates mandatory local law in a certain country, that clause is only invalid in that country, and all other clauses remain valid. The entire license will not be voided due to one problematic clause.

---

## 5. 常见法律疑问解答 / 5. Common Legal FAQ

### Q1：这份许可有法律效力吗？/ Does this license have legal effect?

有。它是一份民事合同，只要你使用了受约束的资产，就视为同意条款，在全球大多数司法辖区都具备民事约束力。具体执行力度会受当地法律影响，但核心规则普遍可执行。

Yes. It is a civil contract. If you use the governed assets, you are deemed to agree to the terms, and it has civil binding force in most judicial jurisdictions worldwide. Specific enforceability may be affected by local laws, but the core rules are generally enforceable.

### Q2：只用了Apache 2.0的源码，会不会触发SPL的付费义务？ / Will using only Apache 2.0 source code trigger SPL payment obligations?

不会。单纯使用、修改、分发源代码，只受Apache 2.0约束，不需要支付SPL费用。只有当你商用了体系逻辑、文本、专利、音乐等创作资产，或者基于本体系开展商业服务时，才适用SPL规则。

No. Simply using, modifying and distributing source code is only subject to Apache 2.0, no SPL fees required. SPL rules only apply when you commercially use creative assets such as system logic, text, patents and music, or provide commercial services based on this system.

### Q3：吹哨人被动取证合法吗？Is passive evidence collection by whistleblowers legal?

合法。取证工具仅分析公开可访问的网络出站流量，不侵入系统、不窃取非公开数据，符合各国网络安全与数据保护的通行规则。

Yes. The forensic tool only analyzes publicly accessible network egress traffic, does not intrude into systems, does not steal non-public data, and complies with general rules of cybersecurity and data protection in various countries.

### Q4：3%的违约金法院会支持吗？ / Will courts uphold the 3% liquidated damages?

设计上已经做了司法适配。首先它被定义为“清算违约金”而非惩罚性罚款；其次条款里明确了对应的损失构成（声誉、维权成本、替代开发成本等），属于合理预估。全球司法实践中，合理约定的违约金通常会得到支持。

Judicial adaptation has been built into the design. First, it is defined as "liquidated damages" rather than punitive penalties; second, the clause clearly specifies the corresponding loss components (reputation, enforcement costs, alternative development costs, etc.), which is a reasonable estimate. In global judicial practice, reasonably agreed liquidated damages are generally upheld.

### Q5：境外企业没有数字人民币账户怎么办？/ What if an overseas enterprise has no e-CNY account?

有三年过渡期，过渡期内正常商用授权费可以用跨境对公支付；只有恶意侵权的违约金才强制数字人民币。过渡期足够企业完成数字人民币账户开立与适配。

There is a three-year transition period. Normal commercial authorization fees can be paid via cross-border corporate payment during the transition period; only liquidated damages for malicious infringement require e-CNY. The transition period is sufficient for enterprises to complete e-CNY account opening and adaptation.

---

**免责声明**：本释义仅为辅助理解之用，不构成法律意见，也不替代正式许可文本。所有法律权利与义务，以QNLOO-SPL主许可及相关法律文件的正式文本为准。

**Disclaimer**: This interpretation is for auxiliary understanding only, does not constitute legal advice, and does not replace the formal license text. All legal rights and obligations shall be subject to the formal text of the QNLOO-SPL master license and related legal documents.

---

**© 2026 千年鹿 QNLOO**

**厦门千年鹿文化科技有限公司 / Xiamen QNLOO Culture & Technology Co., Ltd.**