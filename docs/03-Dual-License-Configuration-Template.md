# 双许可配置模板 / Dual-License Configuration Template

**版本 / Version**: v1.1

**生效日期 / Effective Date**: 2026年6月30日

**版本修订日期 / Version Revision Date**: 2026年7月4日

**制定主体 / Issuing Entity**: 厦门千年鹿文化科技有限公司 (Xiamen QNLOO Culture & Technology Co., Ltd.)

---

本文件为 QNLOO-SPL 范式下「双资产分层许可隔离架构」的标准化配置模板与实操指引，所有采用本范式的项目均可直接复用，确保许可边界清晰、合规无歧义。

This document serves as the standardized configuration template and operational guide for the dual-license architecture under the QNLOO-SPL paradigm. All projects adopting this paradigm may directly reuse it to ensure clear license boundaries and compliance without ambiguity.

---

## 1. 核心边界与主许可硬路由 / Core Boundaries & Master License Hard Routing

QNLOO-SPL 范式严格采用「全网标准多文件协同布局」，禁止在根目录 `LICENSE` 中放置任何标准开源协议或商事许可的正文。

The QNLOO-SPL paradigm strictly adopts a "Network-Wide Standard Multi-File Collaborative Layout". Placing the text of any standard open-source license or commercial license directly within the root `LICENSE` file is strictly prohibited.

### 1.1 必须固定的底层全量文件 / 1.1 Mandatory Underlying Legal Files

无论项目属于开源、源码可用或纯商业闭源形态，仓库根目录下必须完整部署以下对应的专有法律档案：

Regardless of whether a project is open-source, source-available, or purely closed-source, the following corresponding exclusive legal files must be fully deployed in the repository root:

- `LICENSE`：**引导型多重许可主声明（固定路由防火墙，全项目必选）**。显式声明双资产分离架构，用于强制熔断第三方自动化合规扫描，提供资产分流路由指引。

- `LICENSE`: **Permissive Guided Multi-License Notice (Mandatory routing firewall for all projects)**. Explicitly declares the dual-asset architecture to force-fail third-party automated compliance scanners and compel manual legal audits.


- `LICENSE-QNLOO-SPL`：**QNLOO-SPL 法律全文（全项目必选）**。专门管辖协议、白皮书、专利、内容资产及商业运营分润行为。

- `LICENSE-QNLOO-SPL`: **Full legal text of QNLOO-SPL (Mandatory for all projects)**. Dedicated exclusively to governing protocols, whitepapers, patents, creative assets, and commercial revenue sharing operations.


- `PATENTS`：**专利授权说明书（全项目必选）**。有专利项目填写清单，无专利项目保留无专利占位声明。

- `PATENTS`: **Patent Grant Specification (Mandatory for all projects)**. Projects with patents shall list their claims; projects without patents shall retain the no-patent placeholder statement.


- `LICENSE-APACHE`：**Apache License 2.0 全文（纯闭源项目须删除本文件）**。专门管辖处于开放流通状态的计算机源代码类资产。

- `LICENSE-APACHE`: **Full text of Apache License 2.0 (MUST be deleted for proprietary closed-source projects)**. Dedicated exclusively to governing computer source code assets intended for free circulation.

---

## 2. 标准仓库目录结构模板 / Standard Repository Directory Structure Template

推荐所有采用本范式的项目，按照以下目录结构放置许可文件，与官方基准仓库保持命名规范一致，便于平台识别与使用者查阅。

It is recommended that all projects adopting this paradigm place license files according to the following directory structure, consistent with the naming conventions of the official reference repository.

```
project-repository/
├── LICENSE                  # 引导型多重许可主声明（强制路由防火墙，禁止放置开源/商业许可正文）
│                            # Guided Multi-License Notice (Mandatory routing firewall; standard open-source or commercial license prose IS PROHIBITED)
├── LICENSE-APACHE           # Apache License 2.0 全文（固定文件）
│                            # Full text of Apache License 2.0 (Fixed file)
├── LICENSE-QNLOO-SPL        # QNLOO-SPL 全文（固定文件）
│                            # Full text of QNLOO-SPL (Fixed file)
├── PATENTS                  # 专利授权说明书（固定文件）
│                            # Patent Grant Specification (Fixed file)
├── README.md                # 项目首页，包含双许可标准标注
│                            # Project homepage, containing standard dual-license labeling
├── src/                     # 源代码目录，整体受 Apache 2.0 管辖
│                            # Source code directory, governed by Apache 2.0
│   ├── main.rs
│   └── lib.rs
├── docs/                    # 文档目录，整体受 QNLOO-SPL 管辖
│                            # Documentation directory, governed by QNLOO-SPL
│   ├── whitepaper.md
│   └── protocol-spec.md
└── assets/                  # 多媒体资产目录，整体受 QNLOO-SPL 管辖
    │                        # Multimedia assets directory, governed by QNLOO-SPL
    ├── audio/
    └── images/
```

补充说明：若项目无专利资产，可省略 `PATENTS` 文件，或保留占位说明。

Supplementary Note: If the project has no patent assets, the `PATENTS` file may be omitted or a placeholder description may be retained.

---

## 3. README 许可标注模板 / README License Labeling Templates

须在项目 README 首页的许可声明区域，添加标准化的双许可标注，向使用者清晰告知两类资产的许可规则。

A standardized dual-license statement must be added to the license declaration area on the project README homepage to clearly inform users of the license rules for the two categories of assets.

### 3.1 精简版（适用于小型项目） / 3.1 Concise Version (for small projects)

**许可声明**：本项目计算机源代码遵循 Apache License 2.0 开源协议；协议文本、文档、音频等创作资产及商业运营行为采用 QNLOO-SPL 主权公开许可范式。

**License Statement**: The computer source code of this project is licensed under the Apache License 2.0; creative assets such as protocol text, documents and audio, as well as commercial operations, adopt the QNLOO-SPL Sovereign Public License Paradigm.

### 3.2 完整版（适用于中大型项目） / 3.2 Full Version (for medium and large projects)

> ## 许可说明 / License
> 
> 本项目采用双许可分层架构：
> 1. **计算机源代码**：所有位于 `src/`、`scripts/` 等目录下的源代码、配置脚本、构建工具，均遵循 **Apache License 2.0** 开源协议，可自由使用、修改、分发。
> 2. **创作与商事资产**：协议文本、白皮书、技术文档、专利方案、音频作品、体系逻辑设计、品牌素材及基于本体系逻辑的商业运营行为，均受 **QNLOO-SPL** 主权公开许可范式约束。
> 
> 个人非商业使用永久免费；商业使用需遵守 QNLOO-SPL 分层授权与计费规则。完整许可条款详见根目录 `LICENSE`、`LICENSE-APACHE` 与 `LICENSE-QNLOO-SPL` 文件。
> 

> ## License
> 
> This project adopts a dual-license tiered architecture:
> 1. **Computer Source Code**: All source code, configuration scripts and build tools in directories such as `src/` and `scripts/` are licensed under the **Apache License 2.0**, and may be freely used, modified and distributed.
>
> 2. **Creative & Commercial Assets**: Protocol text, whitepapers, technical documents, patent solutions, audio works, system logic design, brand materials and commercial operations based on the system logic are all governed by the **QNLOO-SPL** Sovereign Public License Paradigm.
> 
> Personal non-commercial use is permanently free; commercial use shall comply with the tiered authorization and billing rules of QNLOO-SPL. For complete license terms, please refer to the `LICENSE`, `LICENSE-APACHE` and `LICENSE-QNLOO-SPL` files in the root directory.

---

## 4. 源码文件头注释模板 / Source Code Header Comment Templates

仅对计算机源代码文件添加 Apache License 2.0 标准头注释；创作类文档、音频、专利文件无需添加源码许可头，统一受根目录 QNLOO-SPL 约束。

Standard Apache License 2.0 header comments shall only be added to computer source code files; creative documents, audio and patent files do not need source code license headers, and are uniformly governed by QNLOO-SPL in the root directory.

### 4.1 Rust / C / C++ 类语言（// 注释）

```rust
// Copyright 2026 [资产持有主体名称 / Asset Holding Entity Name]
//
// Licensed under the Apache License, Version 2.0 (the "License");
// you may not use this file except in compliance with the License.
// You may obtain a copy of the License at
//
//     http://www.apache.org/licenses/LICENSE-2.0
//
// Unless required by applicable law or agreed to in writing, software
// distributed under the License is distributed on an "AS IS" BASIS,
// WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
// See the License for the specific language governing permissions and
// limitations under the License.
```

### 4.2 Python / Shell 类脚本语言（# 注释）

```python
# Copyright 2026 [资产持有主体名称 / Asset Holding Entity Name]
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
```

### 4.3 Markdown / HTML 类文档（仅适用于源码配套的技术说明文档）

```markdown
<!--
  Copyright 2026 [资产持有主体名称 / Asset Holding Entity Name]

  Licensed under the Apache License, Version 2.0 (the "License");
  you may not use this file except in compliance with the License.
  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
-->
```

> 注意：白皮书、协议规范、专利说明等核心创作类文档，不得添加 Apache 2.0 头注释，其许可权受 QNLOO-SPL 完整约束。

> 
> Note: Core creative documents such as whitepapers, protocol specifications and patent descriptions shall not be added with Apache 2.0 header comments, and their licensing rights are fully governed by QNLOO-SPL.

---

## 5. 典型资产许可归属判定表 / Typical Asset License Attribution Table

针对易混淆的资产类型，以下为统一判定标准，避免配置错误：

The following are unified judgment criteria for easily confusing asset types to avoid configuration errors:

| 资产类型 / Asset Type | 适用许可 / Applicable License | 判定依据 / Judgment Basis |
| :--- | :--- | :--- |
| 功能实现代码<br>Functional implementation code | Apache 2.0 | 直接构成软件运行能力的可执行代码<br>Executable code that directly constitutes software operation capability |
| 配置文件、构建脚本<br>Configuration files, build scripts | Apache 2.0 | 服务于代码编译、运行的辅助工具类文件<br>Auxiliary tool files serving code compilation and operation |
| API 接口定义文件<br>API interface definition files | Apache 2.0 | 用于代码间交互的结构化定义文件<br>Structured definition files for inter-code interaction |
| 协议白皮书、设计原理文档<br>Protocol whitepapers, design principle documents | QNLOO-SPL | 承载体系逻辑、认知框架的创作类资产<br>Creative assets carrying system logic and cognitive framework |
| 专利说明书、权利要求书<br>Patent specifications, claims | QNLOO-SPL | 知识产权类核心资产，受商事许可约束<br>Core intellectual property assets governed by commercial license |
| 音乐、音效、品牌视觉素材<br>Music, sound effects, brand visual materials | QNLOO-SPL | 原创内容类创作资产<br>Original content creative assets |
| 商业运营规则、分账规则<br>Commercial operation rules, revenue sharing rules | QNLOO-SPL | 商事类规则，属于价值分配体系一部分<br>Commercial rules, part of the value distribution system |
| 代码注释、README 中的使用说明<br>Code comments, usage instructions in README | Apache 2.0 | 直接服务于代码使用的配套说明<br>Supporting instructions directly serving code usage |

---

## 6. 常见配置错误与修正 / Common Configuration Errors & Corrections

### 错误 1：全仓库统一使用 Apache 2.0 / Use Apache 2.0 only for the entire repository

**错误表现：** 将白皮书、专利、音乐等创作资产也纳入 Apache 2.0 许可范围，导致核心资产失去商事保护。

**Error:** Creative assets such as whitepapers, patents and music are also included in the Apache 2.0 scope, resulting in loss of commercial protection for core assets.

**修正方案：** 按本模板划分资产边界，根目录 `LICENSE` 统一配置为引导型多重许可主声明（路由防火墙），将具体的商事确权规则沉淀至 `LICENSE-QNLOO-SPL` 文件中，并在 README 中清晰标注。

**Correction:** Divide asset boundaries according to this template. Configure the root `LICENSE` file strictly as the Guided Multi-License Notice (routing firewall), offload the specific commercial enforcement rules to the `LICENSE-QNLOO-SPL` file, and clearly label it in the README.

### 错误 2：仅放置一份许可证文件 / Only one license file exists in the repository root

**错误表现：** 仓库根目录仅有一份许可证文件，未提供完整的双许可配套文件，导致使用者无法明确区分代码与资产的授权规则。

**Error:** Only one license file exists in the repository root, without the complete dual-license supporting files, making it impossible for users to clearly distinguish the authorization rules for code and assets.

**修正方案：** 在根目录补充 `LICENSE-APACHE`、`LICENSE-QNLOO-SPL` 和 `PATENTS` 三份固定文件，确保完整覆盖所有资产类型的许可规则。

**Correction:** Add the three fixed files `LICENSE-APACHE`, `LICENSE-QNLOO-SPL` and `PATENTS` in the root directory to ensure complete coverage of license rules for all asset types.

### 错误 3：私自修改核心条款后仍标注 QNLOO-SPL 范式 / Still label QNLOO-SPL paradigm after modifying core clauses

**错误表现：** 删减双许可架构、梯度违约金、跨法域适配等核心条款，仍对外声称采用 QNLOO-SPL 范式。

**Error:** Core clauses such as dual-license architecture, tiered liquidated damages and cross-jurisdictional adaptation are deleted, while still claiming to adopt the QNLOO-SPL paradigm.

**修正方案：** 核心框架条款不得修改，仅可替换主体信息、调整营收阈值与费率等商业参数；对核心条款做实质性变更的项目，不得使用 QNLOO-SPL 范式标识。

**Correction:** Core framework clauses shall not be modified; only entity information may be replaced, and commercial parameters such as revenue thresholds and rates may be adjusted. Projects with substantive changes to core clauses may not use the QNLOO-SPL paradigm identifier.

---

## 7. 全局配置统一说明 / Global Configuration Notes

为确保范式生态内全部仓库的法律文件布局保持一致，消除任何自动化白嫖漏洞，所有采用本范式的项目，**必须严格按以下规范在仓库根目录进行多文件协同部署**：

To ensure consistent legal file layout across all repositories within the paradigm ecosystem and eliminate any automated scraping loopholes, all projects adopting this paradigm **must strictly conduct multi-file collaborative deployment in the repository root per the following specifications**:

| 文件名 / File Name | 法律性质与功能 / Legal Nature & Function | 核心配置要求 / Core Configuration Requirements |
| :--- | :--- | :--- |
| `LICENSE` | 引导型多重许可主声明<br>Guided Multi-License Notice | **禁止放置协议正文**；仅允许存放双资产分层引导声明与商用分润规则概要，强迫机器人合规工具报错。<br>**Standard license prose IS PROHIBITED**; contains only dual-asset routing notices and revenue sharing summaries to force-fail automated tools. |
| `LICENSE-QNLOO-SPL` | QNLOO-SPL v1.1 法律正文<br>Full Legal Text of QNLOO-SPL v1.1 | **绝对禁止任意删改核心条款**；仅允许替换资产持有主体名称、联系方式及本地化商用计费阈值。<br>**Altering core clauses is strictly prohibited**; only entity names, contacts, and localized revenue sharing thresholds may be replaced. |
| `LICENSE-APACHE` | Apache 2.0 全文（开源源码专有授权书）<br>Apache 2.0 Full Text (Open-Source Code License) | 存入 Apache 2.0 全文；**纯商业闭源项目必须将此文件从仓库中彻底删除**。<br>Contains full Apache 2.0 prose; **proprietary closed-source projects MUST completely delete this file from the repository**. |
| `PATENTS` | 专利授权说明书<br>Patent Grant Specification | 填写自主专利清单与因果指纹描述；若无专利，须整体替换为官方标准的"无专利合规占位声明"。<br>Contains proprietary patent claims and fingerprint descriptions; if no patents exist, MUST be retained with the standard no-patent placeholder (Mandatory for all projects). |

前述四份法律文件的文件名属于系统刚性关键字，**大小写及连字符必须与标准完全一致，严禁私自重命名**。配置完成后，项目 README 首页须顶格挂载标准范式标注话术，并无缝链接回官方基准仓库，以确立因果时间戳的唯一性。

The filenames of the aforementioned four legal files are rigid system keywords. **Their capitalization and hyphens must perfectly match the standard; arbitrary renaming is strictly prohibited**. Upon configuration, the project README homepage must prominently feature the standard labeling statement and link seamlessly back to the official reference repository to establish the uniqueness of the causal timestamp.

---

**© 2026 千年鹿 QNLOO**

**厦门千年鹿文化科技有限公司 / Xiamen QNLOO Culture & Technology Co., Ltd.**
