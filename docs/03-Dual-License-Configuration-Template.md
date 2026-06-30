# 双许可配置模板 / Dual-License Configuration Template

**版本 / Version**: v1.0

**生效日期 / Effective Date**: 2026年6月30日

**制定主体 / Issuing Entity**: 厦门千年鹿文化科技有限公司 (Xiamen QNLOO Culture & Technology Co., Ltd.)

---

本文件为 QNLOO-SPL 范式下「源码宽松开源 + 创作资产商事许可」双许可架构的标准化配置模板与实操指引，所有采用本范式的项目均可直接复用，确保许可边界清晰、合规无歧义。

This document serves as the standardized configuration template and operational guide for the dual-license architecture of "permissive open-source for source code + commercial license for assets" under the QNLOO-SPL paradigm. All projects adopting this paradigm may directly reuse it to ensure clear license boundaries and compliance without ambiguity.

---

## 1. 核心边界与主许可选择 / Core Boundaries & Master License Selection

QNLOO-SPL 范式采用“三文件固定，一文件按需”的标准化布局。

The QNLOO-SPL paradigm adopts a standardized layout of "three fixed files, one chosen as needed".

### 1.1 必须固定的三个文件（全仓库统一）
### 1.1 Three Mandatory Fixed Files (Uniform Across All Repositories)

| 文件名 / File Name | 内容 / Content | 说明 / Description |
| :--- | :--- | :--- |
| `LICENSE-APACHE` | Apache License 2.0 全文 | 专门对应源代码类资产<br>Dedicated to source code assets |
| `LICENSE-QNLOO-SPL` | QNLOO-SPL v1.0 全文 | 专门对应创作资产与商业运营<br>Dedicated to creative assets & commercial ops |
| `PATENTS` | 专利授权说明书 | 专门对应专利授权<br>Dedicated to patent grants |

### 1.2 主许可的选择（根据仓库属性决定）
### 1.2 Master License Selection (Determined by Repository Attribute)

`LICENSE` 文件的选取，完全遵循“资产决定许可”的物理原则：
The selection of the `LICENSE` file follows the physical principle of "assets determine the license".

| 仓库类型 / Repository Type | 主许可 LICENSE 内容 | 判断逻辑 |
| :--- | :--- | :--- |
| **代码为主的仓库**<br>**Code-dominant repos** | **Apache License 2.0** 全文 | 方便 GitHub 等平台自动识别为“开源项目”<br>For platform auto-recognition as "Open Source" |
| **文本/创作资产为主的仓库**<br>**Text/Creative asset-dominant repos** | **QNLOO-SPL v1.0** 全文 | 确保核心创作资产在商业场景下的权属与分润规则<br>Ensures rights and royalties for core creative assets |

以你的官方仓库为例：

Taking your official repositories as an example:

| 仓库 / Repository | 主许可 LICENSE | 判断原因 |
| :--- | :--- | :--- |
| `01-4-cognition-river-blueprints` | **Apache License 2.0** | 纯代码仓库 |
| `01-1-value-protocols` | **QNLOO-SPL v1.0** | 以协议文本交付为主 |
| `01-2-cognition-river` | **QNLOO-SPL v1.0** | 以白皮书文本交付为主 |
| `01-3-cognition-river-patents` | **QNLOO-SPL v1.0** | 以专利法律文本交付为主 |
| `00-QNLOO-SPL-Licenses` | **Apache License 2.0** | 以工具、模板、源码等构建资产为主 |

---

## 2. 标准仓库目录结构模板 / Standard Repository Directory Structure Template

推荐所有采用本范式的项目，按照以下目录结构放置许可文件，与官方基准仓库保持命名规范一致，便于平台识别与使用者查阅。

It is recommended that all projects adopting this paradigm place license files according to the following directory structure, consistent with the naming conventions of the official reference repository.

```
project-repository/
├── LICENSE                  # 主许可（代码仓库用 Apache 2.0；文本仓库用 QNLOO-SPL）
├── LICENSE-APACHE           # Apache License 2.0 全文（固定文件）
├── LICENSE-QNLOO-SPL        # QNLOO-SPL 全文（固定文件）
├── PATENTS                  # 专利授权说明书（固定文件）
├── README.md                # 项目首页，包含双许可标准标注
├── src/                     # 源代码目录，整体受 Apache 2.0 管辖
│   ├── main.rs
│   └── lib.rs
├── docs/                    # 文档目录，整体受 QNLOO-SPL 管辖
│   ├── whitepaper.md
│   └── protocol-spec.md
└── assets/                  # 多媒体资产目录，整体受 QNLOO-SPL 管辖
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
> **许可声明**：本项目计算机源代码遵循 Apache License 2.0 开源协议；协议文本、文档、音频等创作资产及商业运营行为采用 QNLOO-SPL 主权公开许可范式。
> 
> **License Statement**: The computer source code of this project is licensed under the Apache License 2.0; creative assets such as protocol text, documents and audio, as well as commercial operations, adopt the QNLOO-SPL Sovereign Public License Paradigm.

### 3.2 完整版（适用于中大型项目） / 3.2 Full Version (for medium and large projects)

> ## 许可说明 / License
> 
> 本项目采用双许可分层架构：
> 1. **计算机源代码**：所有位于 `src/`、`scripts/` 等目录下的源代码、配置脚本、构建工具，均遵循 **Apache License 2.0** 开源协议，可自由使用、修改、分发。
> 2. **创作与商事资产**：协议文本、白皮书、技术文档、专利方案、音频作品、体系逻辑设计、品牌素材及基于本体系逻辑的商业运营行为，均受 **QNLOO-SPL v1.0** 主权公开许可范式约束。
> 
> 个人非商业使用永久免费；商业使用需遵守 QNLOO-SPL 分层授权与计费规则。完整许可条款详见根目录 `LICENSE`、`LICENSE-APACHE` 与 `LICENSE-QNLOO-SPL` 文件。
> 

> ## License
> 
> This project adopts a dual-license tiered architecture:
> 1. **Computer Source Code**: All source code, configuration scripts and build tools in directories such as `src/` and `scripts/` are licensed under the **Apache License 2.0**, and may be freely used, modified and distributed.
>
> 2. **Creative & Commercial Assets**: Protocol text, whitepapers, technical documents, patent solutions, audio works, system logic design, brand materials and commercial operations based on the system logic are all governed by the **QNLOO-SPL v1.0** Sovereign Public License Paradigm.
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

### 错误 1：全仓库统一使用 Apache 2.0

错误表现：将白皮书、专利、音乐等创作资产也纳入 Apache 2.0 许可范围，导致核心资产失去商事保护。

Error: Creative assets such as whitepapers, patents and music are also included in the Apache 2.0 scope, resulting in loss of commercial protection for core assets.

修正方案：按本模板划分资产边界，根目录主许可设置为 QNLOO-SPL，仅源代码目录明确适用 Apache 2.0，并在 README 中清晰标注。

Correction: Divide asset boundaries according to this template. Set the main root license to QNLOO-SPL, specify that only the source code directory applies Apache 2.0, and clearly label it in the README.

### 错误 2：仅放置一份许可证文件

错误表现：仓库根目录仅有一份许可证文件，未提供完整的双许可配套文件，导致使用者无法明确区分代码与资产的授权规则。

Error: Only one license file exists in the repository root, without the complete dual-license supporting files, making it impossible for users to clearly distinguish the authorization rules for code and assets.

修正方案：在根目录补充 `LICENSE-APACHE`、`LICENSE-QNLOO-SPL` 和 `PATENTS` 三份固定文件，确保完整覆盖所有资产类型的许可规则。

Correction: Add the three fixed files `LICENSE-APACHE`, `LICENSE-QNLOO-SPL` and `PATENTS` in the root directory to ensure complete coverage of license rules for all asset types.

### 错误 3：私自修改核心条款后仍标注 QNLOO-SPL 范式

错误表现：删减双许可架构、梯度违约金、跨法域适配等核心条款，仍对外声称采用 QNLOO-SPL 范式。

Error: Core clauses such as dual-license architecture, tiered liquidated damages and cross-jurisdictional adaptation are deleted, while still claiming to adopt the QNLOO-SPL paradigm.

修正方案：核心框架条款不得修改，仅可替换主体信息、调整营收阈值与费率等商业参数；对核心条款做实质性变更的项目，不得使用 QNLOO-SPL 范式标识。

Correction: Core framework clauses shall not be modified; only entity information may be replaced, and commercial parameters such as revenue thresholds and rates may be adjusted. Projects with substantive changes to core clauses may not use the QNLOO-SPL paradigm identifier.

---

## 7. 全局配置统一说明 / Global Configuration Notes

为确保范式生态内全部仓库的法律文件布局保持一致，所有采用本范式的项目，**必须在仓库根目录同时部署四份法律文件**：

To ensure consistent legal file layout across all repositories within the paradigm ecosystem, all projects adopting this paradigm **must deploy four legal files simultaneously in the repository root directory**:

| 文件名 / File Name | 内容 / Content | 适用资产 / Applicable Assets |
| :--- | :--- | :--- |
| `LICENSE` | Apache License 2.0 或 QNLOO-SPL（二选一） | 仓库主要资产的主许可<br>Master license for primary assets |
| `LICENSE-APACHE` | Apache License 2.0 全文（固定） | 源代码类资产<br>Source code assets |
| `LICENSE-QNLOO-SPL` | QNLOO-SPL v1.0 全文（固定） | 创作资产与商业运营<br>Creative assets & commercial ops |
| `PATENTS` | 专利授权说明书（固定） | 专利授权<br>Patent grants |

上述四份文件的文件名严格固定，不得重命名。这确保了无论是通过 GitHub 等平台的自动识别，还是人工查阅，都能立即确定仓库的法律状态。

The filenames of the above four files are strictly fixed and must not be renamed. This ensures that the legal status of the repository can be immediately determined, whether through automatic identification by platforms such as GitHub or manual review.

配置完成后，建议在项目 README 中添加指向 QNLOO-SPL 官方基准仓库的链接，表明范式来源，便于使用者查阅标准规则。

After configuration, it is recommended to add a link to the official QNLOO-SPL reference repository in the project README to indicate the paradigm source and facilitate users to access standard rules.

---

**© 2026 千年鹿 QNLOO**

**厦门千年鹿文化科技有限公司 / Xiamen QNLOO Culture & Technology Co., Ltd.**
