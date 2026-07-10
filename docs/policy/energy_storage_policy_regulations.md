# 储能行业政策法规汇总

> 最后更新：2026-07-11
> 覆盖地区：欧洲（全覆盖）、澳大利亚

**适用品类标记说明：**

| 标记 | 含义 |
|------|------|
| `[家储]` | 家庭储能（Home Storage） |
| `[阳储]` | 阳台储能（Balcony Storage / Balkonkraftwerk） |
| `[移储]` | 便携/移动储能（Portable Power Station） |
| `[工商储]` | 工商业/公用级储能（C&I / Utility-scale BESS） |
| `[通用]` | 适用所有储能品类 |

**常用单位说明：**

| 单位 | 全称 | 度量 | 说明 | 政策中的典型用法 |
|------|------|------|------|----------------|
| **kWp** | kilowatt-peak（千瓦峰值） | 功率 | 光伏组件在标准测试条件下的最大发电功率 | ">2 kWp"界定光伏系统规模（如 Solarspitzengesetz 门槛） |
| **kWh** | kilowatt-hour（千瓦时） | 能量 | 一段时间内实际产生或存储的电量（= 1 度电） | ">2 kWh"界定电池容量（如 EU 电池法规碳足迹申报门槛） |
| **kW** | kilowatt（千瓦） | 功率 | 设备的实时输入/输出功率 | "800W 馈电上限"限制逆变器向电网输出的最大功率 |
| **Wp** | watt-peak（瓦峰值） | 功率 | kWp 的千分之一，用于描述单块光伏组件 | "2000 Wp 组件上限"限制阳台光伏的模组总功率 |

> **简单记忆：kWp 管光伏板大小，kWh 管电池容量，kW/W 管实时功率。**

---

## 一、欧盟层面

### 1.1 EU 电池法规（EU Battery Regulation 2023/1542）`[通用]`

#### 总体时间线

| 里程碑 | 内容 | 生效时间 |
|--------|------|---------|
| CE 标识强制 | 所有在 EU 销售的电池必须完成 CE 认证 | 2024-08-18 |
| EPR 注册 | 所有电池生产商必须完成 EPR（生产者延伸责任）注册 | 2025-08-18 |
| 电池护照 | 所有 >2 kWh 工业电池必须附带数字"电池护照"（Battery Passport），含成分、碳足迹、可回收性 | 2027-02-18 |

#### 碳足迹申报（Carbon Footprint Declaration）— 三阶段递进

碳足迹要求按"申报→分级→准入门槛"三阶段递进实施，不同电池品类适用不同时间线：

**阶段一：碳足迹申报（Carbon Footprint Declaration）**

| 电池品类 | 适用储能产品 | 申报启动时间 |
|---------|-------------|-------------|
| EV 电池 | — | 2025-02-18 |
| >2 kWh 可充电工业电池 | `[家储]` `[阳储]`（多数 >2 kWh） | 2026-02-18 |
| LMT 电池（轻型交通工具） | `[移储]`（部分便携储能可能归入此类） | 2028-02-18 |

- 申报内容：基于 **PEF（产品环境足迹）方法论** 的全生命周期碳排放，覆盖原材料开采→活性材料制造→电芯制造→电池组装→分销→报废处理全链路
- 计算标准：遵循 ISO 14040/44（LCA 框架）和 ISO 14067（碳足迹量化），采用 EU PEF Category Rules (PEFCR)
- 度量单位：**kg CO₂e / kWh**（每千瓦时全生命周期交付能量的二氧化碳当量）
- 申报格式：欧盟委员会于 `[2024-04]` 发布了委托法规（Delegated Regulation）和实施法规（Implementing Regulation），规定了标准化的申报模板和计算步骤
- 需经**第三方验证**

**阶段二：碳足迹性能等级标签（Performance Class Labeling）**

| 电池品类 | 等级标签启动时间 |
|---------|----------------|
| EV 电池 | 2026-02-18 |
| >2 kWh 可充电工业电池 | 2026-08-18 |
| LMT 电池 | 2028-08-18 |

- 类似能效标签（A/B/C/D…），A 级代表最低碳足迹
- 等级划分基于市场已申报碳足迹的分布基准
- 标签必须**清晰、可读、永久标注**在电池本体上

**阶段三：碳足迹准入上限（Maximum Carbon Footprint Threshold）**

| 电池品类 | 上限生效时间 |
|---------|-------------|
| EV 电池 | 2027-07（委托法规） |
| >2 kWh 可充电工业电池 | 待定（预计 2028 后） |

- 欧盟委员会将设定**每种电池类型的最高允许碳足迹**
- **超过上限的电池将被禁止在 EU 市场销售**
- 这是最终的硬性准入门槛

#### 数字电池护照（Digital Battery Passport）

| 要求 | 说明 |
|------|------|
| **适用范围** | EV 电池 + >2 kWh 可充电工业电池 `[家储]` `[阳储]` |
| **生效时间** | 2027-02-18 |
| **唯一标识** | 每块电池分配唯一标识码（Unique Identifier） |
| **QR 码** | 必须在电池本体上印刷或刻蚀 QR 码，链接至数字护照 |
| **数据可用性** | 数据必须在电池整个服务寿命期间保持准确、安全、可访问（10-15 年+） |
| **数据模型** | 基于 AAS（Asset Administration Shell）和 SAMM（Semantic Aspect Meta Model）标准 |
| **技术生态** | Battery Pass 联盟 + GBA（全球电池联盟）+ Catena-X 数据生态 |
| **数据分层** | 公开数据（碳足迹、成分、可回收性）vs 受控数据（IP 相关的制造细节） |

- **影响**：`[通用]` 对所有储能产品的 BOM 管理、供应链溯源、产品合规认证提出系统性要求。便携储能同样受制于 CE 认证和 EPR 注册要求

### 1.2 净零工业法案（Net-Zero Industry Act）`[通用]`

- `[2024-06 通过]` 储能项目可享受简化审批流程和国家援助对齐
- 强调供应链韧性和战略自主

### 1.3 关键原材料法案（Critical Raw Materials Act）`[通用]`

- `[2024-05 通过]` 对锂、钴、镍等关键原材料的供应链多元化提出要求
- 影响电芯采购策略和成本结构

### 1.4 EU BESS 合规与安全标准 `[通用]`

| 标准/指令 | 适用范围 | 说明 |
|-----------|---------|------|
| CE 认证 | `[通用]` | EU 市场准入强制标识 |
| EMC 指令 | `[通用]` | 电磁兼容性 |
| 低电压指令（LVD） | `[通用]` | 电气安全 |
| IEC 62619 | `[家储]` `[阳储]` | 工业锂电池安全标准 |
| IEC 62133 | `[移储]` | 便携式锂电池安全标准 |
| EN 62040 | `[家储]` | UPS 标准 |
| EN 50549 | `[家储]` `[阳储]` | 并网设备要求 |
| RoHS 指令 | `[通用]` | 有害物质限制 |
| REACH 法规 | `[通用]` | 化学品注册与评估 |

> **来源：**
> - [EU and UK Energy Storage Regulation in 2026 and Beyond — Morgan Lewis](https://www.morganlewis.com/pubs/2026/03/eu-and-uk-energy-storage-regulation-in-2026-and-beyond) `[2026-03]`
> - [EU Regulations for BESS: Compliance & Safety Guide 2026 — SunLit Energy](https://sunlithenergy.com/eu-regulations-for-battery-energy-storage-systems/) `[2026]`
> - [Energy Storage Battery Certifications in Europe — Battlink](https://battlink.com/news/energy-storage-battery-certifications-in-europe/) `[2025]`
> - [Portable Energy Storage Certification Guide — GDESTL](https://en.gdestl.com/588.html) `[2025]`
> - [EU Members Mixed Progress on Energy Storage — Energy Storage News](https://www.energy-storage.news/european-union-members-make-mixed-progress-in-implementing-energy-storage-strategies/) `[2025-04]`

### 1.5 电池法规近期实施节点 `[通用]`

#### 2026-08-18 标注新要求 `[即将生效]`

EU 电池法规第二阶段标注强制要求将于 2026-08-18 落地：

| 要求 | 说明 |
|------|------|
| **制造商标注** | 制造商信息、化学成分、重量、容量、制造日期、预期寿命 |
| **不可充电电池** | 须加贴专用符号 |
| **EV 电池** | 须在标签上显示碳足迹数据 |
| **小体积电池** | 信息可在包装或随附文件上体现 |

#### 电池护照委托法规 `[待发布]`

欧盟委员会须在 **2026-08-18** 前发布委托法规（Delegated Act），规定数字电池护照的数据访问权限（公开 vs 受控分层）及信息录入、修改和更新规则。供应链尽职调查实施指南发布时间已明确为 **2026-07-26**，较原计划推迟超一年；与此同时，钴、锂、镍等关键原材料的尽职调查强制执行日期本身也已从原定 2025-08-18 整体推迟至 **2027-08-18**，为企业供应链溯源体系建设留出更长窗口。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2024-04 | 碳足迹申报委托法规和实施法规发布 |
| 2026-02-18 | >2 kWh 工业电池碳足迹申报生效 |
| **2026-07-26（预计）** | **供应链尽职调查实施指南发布（较原计划推迟逾一年）** |
| **2026-08-18** | **标注新要求生效 + 电池护照委托法规发布 + 碳足迹性能等级标签启动** |
| 2027-02-18 | 数字电池护照强制生效 |
| **2027-08-18** | **尽职调查义务正式强制执行（较原计划 2025-08-18 推迟两年）** |

> **来源：**
> - [EU Battery Regulation 2026: What Retailers Must Know — Impala Services](https://www.impala-services.com/blog/eu-battery-regulation-technical-documentation-retailers) `[2026]`
> - [EU Battery Passport Regulation: What You Need to Know in 2026 — Base Battery Passport](https://base-batterypassport.com/blog/regulations-4/eu-battery-passport-regulation-57) `[2026]`
> - [DPP Timeline 2026-2030: Every Deadline — PassportCraft](https://passportcraft.com/insights/dpp-timeline-2026-2030-every-deadline) `[2026]`
> - [EU Battery Regulation Due Diligence Rules: what next in the implementation — The Environment Coalition](https://te-cdn.ams3.cdn.digitaloceanspaces.com/files/Due-diligence-guidance-for-the-Battery-Reg-1.pdf) `[2026-07]`

### 1.6 电力市场灵活性评估 `[通用]`

**政策正文概述：** 根据 EU 电力市场设计（Electricity Market Design）改革要求，ACER 已于 2025-07 批准欧盟统一的非化石灵活性需求评估方法论。各成员国须在 **2026-07 前**完成并提交国家灵活性评估报告，并于 **2027-01 前**设定包含储能子目标的非化石灵活性指示性目标。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025-07 | ACER 批准统一灵活性评估方法论 |
| **2026-07** | **各成员国提交灵活性评估报告** |
| **2027-01** | **各成员国设定储能子目标** |
| 2027-07 | ACER 发布欧盟层面汇总报告 |

> **来源：**
> - [ACER approves EU-wide methodology to assess national electricity flexibility needs — ACER](https://www.acer.europa.eu/news/acer-approves-eu-wide-methodology-assess-national-electricity-flexibility-needs) `[2025-07]`
> - [EU energy flexibility trends 2026 — electron.net](https://electron.net/energy-flexibility-trends-updates-european-union-eu/) `[2026]`

### 1.7 工业加速法案（Industrial Accelerator Act） `[通用]` `[立法进行中]`

**政策正文概述：** 欧盟委员会于 2026-03-04 发布 IAA 草案，对受公共资金支持的净零技术采购（含补贴发放和竞标拍卖）引入分阶段 Made in Europe 含量要求。覆盖电池、BESS、光伏、热泵、风电等净零技术。法案仍在 EU 立法程序中，尚未正式生效。

**BESS 欧产含量要求：**

| 阶段 | 时间点 | 要求 |
|------|--------|------|
| 第一阶段 | 法案生效后 **1 年** | >1 MWh 系统须采用欧盟制造的 **BMS** |
| 第二阶段 | 法案生效后 **3 年** | 须额外采用欧盟制造的**电池电芯**及至少一个主要部件 |

行业协会（Energy Storage Europe）警告：若时间表过紧，将在储能扩张最急迫阶段反而放慢 BESS 部署。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-03-04 | 欧盟委员会发布 IAA 立法提案 |
| **2026-Q2** | **欧洲议会指定报告人（Rapporteur），正式启动议会审议程序** |
| **2027 年以后（预计）** | **立法流程完成（欧盟议会 + 理事会联合决策，通常需 1-2 年）** |

> **来源：**
> - [EU industrial strategy could slow BESS progress, association warns — ESS News](https://www.ess-news.com/2026/03/05/eu-industrial-strategy-could-slow-bess-progress-association-warns/) `[2026-03]`
> - [EU Industrial Accelerator Act — Bird & Bird](https://www.twobirds.com/en/insights/2026/europe-powers-up-the-eu's-bold-legislative-drive-for-a-homegrown-battery-industry) `[2026]`
> - [Industrial Accelerator Act: EU Legislation in Progress — European Parliament Think Tank](https://epthinktank.eu/2026/05/21/industrial-accelerator-act-eu-legislation-in-progress/) `[2026-05]`

### 1.8 EU 储能部署三方协议（Tripartite Agreement）`[通用]`

#### 首个储能行业三方协议签署 `[已签署]`

**政策正文概述：** 欧盟委员会于 **2026-06-26** 签署首个储能行业三方协议，22 个成员国承诺在 **2026-2028** 两年间新增 **30-35 GW** 储能容量。协议核心目标：① 储能配套 PPA 规模从 2026 年 1.5 GW 增至 2028 年 **4.5 GW**；② 工商业 BESS 容量从 9 GWh 增至 **24 GWh**；③ 工业热储能从 0.5 GWh 增至 **1.5 GWh**。背景：EU 截至 2025 年底已装机约 55 GW（同比 +45%），距 2030 年 200 GW 目标缺口约 145 GW，三方协议是 EU 加速弥合这一缺口的首个政治承诺工具。EIB 集团同步宣布为协议提供融资支持。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-06-26 | 欧盟委员会宣布首个储能三方协议，22 个成员国签署，承诺 30-35 GW（2026-2028） |

> **来源：**
> - [EU tripartite agreement targets 30-35GW of storage deployments by 2028 — Energy-Storage.News](https://www.energy-storage.news/eu-tripartite-agreement-targets-30-35gw-of-storage-deployments-by-2028/) `[2026-06]`
> - [First-ever EU tripartite agreement signed to boost energy storage — European Commission](https://ec.europa.eu/commission/presscorner/detail/en/ip_26_1426) `[2026-06]`
> - [Energy storage: EIB Group supports EU tripartite initiative — EIB](https://www.eib.org/en/press/news/news-energy-storage-eib-group-supports-eu-tripartite-initiative) `[2026-06]`

### 1.9 应急能源工具箱（AccelerateEU）`[通用]`

#### 委员会通信文件发布，行业协会批评储能配套措施不足 `[已发布]`

**政策正文概述：** 欧盟委员会于 **2026-04-22** 发布"AccelerateEU——能源联盟：通过加速行动实现可负担与安全能源"通信文件，是对 2026-03-19 欧洲理事会结论（应对伊朗危机及霍尔木兹海峡中断风险）的直接回应，旨在降低能源价格波动和对化石燃料的结构性依赖。文件重申 EU 到 2030 年储能容量需扩展至约 **200 GW** 的量级目标，并提出设定"电气化目标"（electrification target）。行业协会普遍认可方向但批评落地力度不足：SolarPower Europe 指出文件"未能提出实现该储能规模的具体措施"；Flow Batteries Europe 批评文件仅提及短时 BESS 和抽水蓄能，**再次忽略长时储能（LDES）**这一"关键工具"，警告欧洲可能重蹈此前政策空白的覆辙。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-03-19 | 欧洲理事会结论要求委员会提出应对能源危机的加速行动 |
| **2026-04-22** | **欧盟委员会发布 AccelerateEU 通信文件，设定 200 GW 储能量级目标、电气化目标** |
| **2026-04（随后）** | **SolarPower Europe、Flow Batteries Europe 等行业协会发表批评声明，指出缺乏具体 BESS/LDES 落地措施** |

> **来源：**
> - [AccelerateEU to strengthen EU energy resilience — European Commission](https://energy.ec.europa.eu/strategy/accelerateeu-strengthen-eu-energy-resilience_en) `[2026-04]`
> - [AccelerateEU 'emergency toolbox' policy on fossil fuel dependence falls short on energy storage, trade groups say — Energy-Storage.News](https://www.energy-storage.news/accelerateeu-emergency-toolbox-policy-on-fossil-fuel-dependence-falls-short-on-energy-storage-trade-groups-say/) `[2026]`
> - [Statement: European Commission adopts its emergency toolbox 'AccelerateEU' — SolarPower Europe](https://www.solarpowereurope.org/press-releases/statement-european-commission-adopts-its-emergency-toolbox-accelerate-eu) `[2026-04]`
> - [EU launches toolbox to accelerate clean energy, falls short on energy storage — PV Tech](https://www.pv-tech.org/eu-launches-toolbox-to-accelerate-clean-energy-falls-short-on-energy-storage/) `[2026-04]`

### 1.10 电池法规简化提案（Omnibus）`[通用]` `[立法进行中]`

#### 可拆卸性豁免委托法案草案 `[草案]`

**政策正文概述：** 欧盟委员会于 2026-04-28 正式发布 EU 电池法规（EUBR）第 11 条"终端用户可拆卸/可更换电池设计要求"的豁免委托法案（Delegated Act）草案，作为 Omnibus 简化一揽子计划的一部分，公众意见征询于 **2026-05-26** 截止。草案拟新增六类产品豁免，含可穿戴设备（智能手表、健身追踪器）、电动玩具、ATEX 指令适用设备（防爆电机、传感器、泵、叉车等）；可穿戴设备豁免为"部分豁免"——允许专业维修人员（而非终端用户）拆卸更换电池。同步推进的 Omnibus 提案还包括：修改远程销售场景下的生产者定义、新增高关注物质（SVHC）标签要求、LMT 电池包排除出可拆卸性/可更换性适用范围、放宽数据审查频率要求。立法目标是在 **2026 年底前**完成，这是利益相关方在第 11 条 2027-02 强制生效前就适用范围发声的**最后窗口**。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-04-28 | 委员会发布可拆卸性豁免委托法案草案，公众征询启动 |
| **2026-05-26** | **公众征询截止** |
| **2026 年底（目标）** | **Omnibus 简化一揽子计划立法程序完成** |
| 2027-02-18 | 第 11 条可拆卸/可更换要求强制生效（豁免范围最终版须在此前明确） |

> **来源：**
> - [Commission seeks views on battery removability exemptions — European Commission](https://environment.ec.europa.eu/news/commission-seeks-views-battery-removability-exemptions-2026-04-28_en) `[2026-04]`
> - [EU Batteries Regulation: Commission Proposes New Exemptions from End-User Battery Removability Requirements — Cooley](https://products.cooley.com/2026/05/15/eu-batteries-regulation-european-commission-proposes-new-exemptions-from-end-user-battery-removability-requirements/) `[2026-05]`
> - [Batteries: EU proposes simpler removability and replacement rules — ERP Global](https://erp-recycling.org/news-and-events/2026/04/batteries-eu-proposes-simpler-removability-and-replacement-rules/) `[2026-04]`

#### PM 解读

> **[2026-07-03]**
>
> - 碳足迹合规是 2026-2027 年 EU 市场准入的**第一优先级事项**。不做 = 退出 EU 市场（无碳足迹申报 → 无 CE 认证 → 产品禁售）
> - 碳足迹合规不是"填个表"，而是需要**六层软件系统全链路贯通**的系统工程：供应链数据采集 → LCA 计算引擎 → 电池护照平台 → BMS 固件改造 → 云平台扩展 → App 端展示
> - 关键节点：>2 kWh 产品碳足迹申报已于 2026-02 生效（已逾期），性能等级标签 2026-08 启动，电池护照 2027-02 强制生效
> - `[家储]` 全面受影响（市场主力 5-15 kWh 全部 >2 kWh）；`[阳储]` 多数受影响（需逐一确认 2 kWh 边界）；`[移储]` 推迟至 2028，但大容量产品（如 DELTA Pro 3.6 kWh）需提前合规
> - 性能等级标签（A/B/C/D）将成为新的竞争分层维度，LFP 路线在碳足迹等级上可能占优
> - IEC 62133 vs IEC 62619 标准分野意味着不同产品线的 BMS 固件安全逻辑不能简单复用
> - **2026-08-18 委托法规是电池护照系统设计的最后一块拼图**：委托法规将明确护照数据访问权限分层（谁可以看哪些字段）和信息更新规则。这是构建电池护照软件系统的关键输入——访问权限划分决定前端角色 UI 设计（不同身份可见字段不同），更新规则决定数据管道架构（谁能写入、谁能只读、何时触发更新）。2026-08-18 发布后应立即解读并同步更新系统设计，距 2027-02 电池护照强制生效仅剩约 6 个月
> - **IAA 欧产含量要求是中国厂商参与 EU 公共补贴项目的新隐性门槛——BMS 欧产要求 1 年内落地，需立即评估合规路径**：IAA 草案对公共资金支持的储能项目设定分阶段欧产要求（1 年：BMS；3 年：电芯）。德国 KfW 补贴、英国 Warm Homes Plan、意大利 GSE 计划等主要公共补贴项目均可能纳入 IAA 范围，意味着中国储能厂商若无欧洲制造的 BMS，可能在法案生效 1 年后失去上述补贴项目的产品资格。建议立即启动两项评估：① 现有 BMS 供应商是否可以切换至欧洲制造版本（或合作欧洲供应商）；② IAA 正式生效时间线（立法程序约 1-2 年），对应产品供应链改造窗口。Northvolt 破产后欧洲电芯产能高度受限，3 年电芯欧产要求若不放宽，实际上对所有非欧洲厂商构成系统性障碍
> - **IAA 立法进度更新：已进入议会审议阶段，最终立法预计 2027 年以后**：欧洲议会已于 2026-Q2 完成报告人（Rapporteur）指派，正式启动议会审议程序。欧盟理事会与议会联合决策流程通常需 1-2 年，实际生效最早 2027 年。这意味着：① 针对 IAA Made in Europe 要求的供应链合规窗口仍有 1-2 年缓冲；② 当前是提交行业意见、争取条款宽松化的最佳时机（议会磋商阶段比立法完成后更容易影响文本）；③ BMS 欧产要求虽尚未生效，但 IAA + StromVKG ≥50% EEA 要求同向叠加——欧洲制造布局的战略必要性已从"未来选项"升格为"现在决策"
> - **EU 首签储能三方协议（30-35 GW / 2028），政治承诺升格为可量化市场信号——C&I BESS 从 9 GWh 到 24 GWh 是最直接的 B 端机会窗口**：三方协议是 EU 首次以可量化目标（GW/GWh）公开承诺储能规模化部署，并将 C&I BESS 扩容 2.7 倍（9 → 24 GWh）作为明确子目标。对产品策略的含义：① C&I 储能是欧洲层面政策支持最清晰的细分市场，2026-2028 是大型 BESS 的窗口期；② 储能配套 PPA 目标从 1.5 GW 增至 4.5 GW，意味着 B 端能源管理平台需要具备 PPA 合规运营功能（确保 BESS 在 PPA 合约框架内按约交付，并提供符合买方核查要求的可信数据）；③ EIB 融资支持为三方协议的落地提供了信用背书，储能厂商可借助 EIB 融资渠道降低欧洲 B 端项目的资本成本
> - **AccelerateEU 重申 200 GW 储能目标但缺乏具体落地措施，行业协会的批评揭示了政策与市场之间的执行缺口，这是产品出海节奏判断的重要参考信号**：委员会 2026-04 发布的应急能源工具箱重申了储能规模化的必要性，但 SolarPower Europe 和 Flow Batteries Europe 均批评其"只有目标、没有配套措施"，且完全未提及长时储能。对产品策略的含义：① 短时 BESS/家储仍是 EU 政策关注和支持的主战场，长时储能（LDES）产品线短期内不应指望 EU 层面的专项政策拉动，需求驱动仍主要依赖英国 Ofgem LDES Cap & Floor 等成员国级别机制（见 7.6）；② "目标先行、措施滞后"的模式意味着 EU 层面的储能政策利好更多是市场信心信号而非可直接变现的补贴或强制配额，产品出海优先级判断应更依赖三方协议（1.8）等已有具体量化承诺的工具，而非停留在通信文件层面的表态
> - **可拆卸性豁免草案对储能产品线本身影响有限，但释放了"Omnibus 简化窗口内可争取条款松绑"的信号，应同步评估电池护照数据颗粒度是否有类似松绑空间**：草案聚焦可穿戴设备、玩具、ATEX 设备等消费电子/工业专用品类，家储/阳储/移储主力产品（>2 kWh 电池组）不在拟豁免范围内，第 11 条可拆卸性要求对储能产品的适用性预期不变。但该草案证明 Omnibus 简化一揽子计划确实在实质性调整 EUBR 细则（如 LMT 电池包排除可拆卸性适用、数据审查频率放宽），且 2026 年底前是最后立法窗口。建议：① 通过 Energy Storage Europe/BVES 等行业协会评估电池护照数据模型（1.1/1.5）是否有类似"简化数据颗粒度或更新频率"的游说空间；② 密切跟踪 2026 年底 Omnibus 立法收尾进展，避免临近 2027-02 强制生效前才发现细则变化
>
> **详细分析见 → [EU 碳足迹合规专题分析](eu_carbon_footprint_compliance_analysis.md)**（含六层架构拆解、不合规四级影响链路、产品线差异化影响、竞争格局分析、行动时间表）

---

## 二、德国

### 2.1 家庭储能补贴 `[家储]`

**KfW（Kreditanstalt für Wiederaufbau，德国复兴信贷银行）** 是德国政府全资持有的政策性银行，是推动家庭光储普及的核心政策工具。

| 项目 | 内容 | 时间 |
|------|------|------|
| **KfW 270** | "可再生能源标准贷款"，覆盖与光伏配套的储能系统，最高可贷 100% 合格费用（含电池、逆变器、安装、规划），有效年利率低至 3.27% | 持续有效 |
| **KfW 442** | 补贴最高 €3,200，适用于光伏+储能组合（最低 5 kWh） | 持续有效 |
| **巴伐利亚州** | Solar Storage Bonus：€500–€1,250（按储能容量） | 2025 年有效 |
| **北威州（NRW）** | Battery Voucher：€150/kWh，最高 10 kWh | 2025 年有效 |

- **申请要点**：KfW 270 必须在签署采购合同前通过开户银行（Hausbank）提交申请
- **渠道影响**：安装商帮用户申请 KfW 补贴时需提交产品合规文件（CE 认证、技术规格书、安全测试报告等），合规文档包不齐全的品牌会被安装商直接放弃——KfW 合规文档包是进入德国家储渠道的前置条件

### 2.2 税收优惠 `[家储]` `[阳储]`

- `[2023-01 起]` **0% 增值税**：适用于储能硬件及安装服务（含家储和阳台储能设备）

### 2.3 馈电政策 `[家储]`

- `[2025-02]` **Solarspitzengesetz（太阳能峰值法）生效**：所有 >2 kWp 新系统在 EPEX 现货价格为负的任何 15 分钟区间内，馈电补偿为零；新系统馈电功率限制为 60%（除非安装智能电表）；>2 kWp 新系统强制安装智能电表（iMSys）
- `[2025-04]` **§14a EnWG Modul 3 生效**：分时动态电网费（高/中/低三档），可控负载设备可节省超过 12 ct/kWh 电网费价差
- `[2026-08-01 即将生效]` **EEG 馈电补偿半年递减**：EEG 2023 内置的半年 1% 递减机制（每年 2 月 1 日 / 8 月 1 日）将于 2026-08-01 再次触发；新并网系统馈电补偿区间从当前约 5.50–12.35 ct/kWh 降至约 **5.45–12.22 ct/kWh**（部分馈电至全额馈电，按系统规模）。进一步弱化纯光伏（未配储能）新系统的 ROI，与 EEG 2027 改革方向叠加，储能配套的经济刚需持续强化
- `[2026-12]` EEG 2023 国家援助审批到期，德国正推动从固定馈电补贴转向市场化机制
- **影响**：配储能的系统可规避负电价窗口，储能配套从"锦上添花"变为"经济性刚需"

> **来源（EEG 半年递减）：**
> - [Einspeisevergütung 2026: Senkung am 1. August + EEG-Reform 2027 — reduco.ai](https://reduco.ai/blog/einspeiseverguetung-aenderungen-2026-2027) `[2026-06]`
> - [Feed-in tariff 2025/2026: amount, profitability, innovations — autarc.energy](https://www.autarc.energy/global/knowledge/einspeisevergutung) `[2026]`

**详细分析见 → [德国馈电政策专题分析](germany_feed_in_policy_analysis.md)**（含 EMS 算法需求、§14a 动态电网费、VPP 生态、竞品对标、四层软件架构拆解、分阶段实施路线）

**负电价趋势** `[持续恶化]`

德国负电价小时数持续攀升，日间 10:00-15:00 集中出现，太阳能捕获系数（solar capture factor）同步下滑。配储能系统可规避负电价窗口。

| 年份 | 负电价小时数 | 同比 | 太阳能捕获系数（4月） |
|------|-------------|------|----------------------|
| 2025 | 576 小时 | +26% | ~0.40 |
| 2026 | ~864 小时（估） | ~+50% | ~0.26（跌幅约 1/3） |

**H1 2026 补充数据：** 德国上半年光伏发电量 43.2 TWh（同比 +10%，历史新高）；同期光伏弃光（curtailment）约 3 GWh，其中 **58.2%** 集中发生在日前电价为负的时段——负电价窗口下的弃光占比首次成为主导因素，进一步验证储能配置对捕获率（capture rate）的直接提升作用。

> **来源：**
> - [Germany Power Prices Turn Deeply Negative — Bloomberg](https://www.bloomberg.com/news/articles/2026-04-07/germany-power-prices-turn-deeply-negative-on-renewables-surge) `[2026-04]`
> - [Solar Capture Factors Fall Across Europe — PV Magazine](https://www.pv-magazine.com/2026/05/13/solar-capture-factors-fall-across-europe-as-negative-price-hours-surge-in-key-markets/) `[2026-05]`
> - [Germany solar PV generation up 10% year-on-year in H1 2026 — PV Tech](https://www.pv-tech.org/germany-solar-pv-generation-increases-h1-2026/) `[2026-07]`

**EEG 2027 改革（Referentenentwurf）** `[立法进行中]`

BMWK 于 2026-02-27 发布 442 页草案，核心条款：① 2027-01-01 起，新建 <25 kWp 住宅光伏系统取消固定 EEG 馈电补偿（Einspeisevergütung），全部强制转向市场化 Direktvermarktung；② 小型光伏系统设定 50% 馈电功率永久上限，配储能系统可豁免；③ 强制安装 iMSys 的装机门槛从 7 kW 降至 2 kW；④ 屋顶光伏拍卖规模从 2,300 MW/年削减至 1,500 MW/年（2027-2032），地面电站从 9,900 MW 扩大至 14,000 MW；⑤ 草案同时提出加大电池储能投资激励，定位储能为光伏标准配置。若取消固定馈电补偿且无替代机制，典型 10 kW 系统投资回收期将从 15.6 年骤增至 30 年以上。

> **进展追踪**
> - `[2026-02-27]` BMWK 发布部级草案（Referentenentwurf），442 页，尚未进入正式立法程序
> - `[2026-06-10]` 原定内阁表决未进行，经济部与环境部在 Redispatch 条款及 ≤25 kWp 馈电补偿问题上存在分歧
> - `[2026-06-10]` Reiche 在 BDEW 年会承诺夏休前提交内阁，明确放弃 Redispatch 预留条款（关键妥协信号）
> - `[2026-06-15]` 新目标表决日期调整为 2026-06-24
> - `[2026-06-19]` 内阁表决再度推迟至 7 月，具体日期未定（"Ein konkretes Datum gibt es nicht"）；Netzpaket 同步延后
> - **`[2026-07-01]`** **距夏休仅剩两周，经济部（Reiche）与环境部（Schneider）仍无进展，内阁表决日期依旧未定；Schneider 重申不会同意任何"危及可再生能源扩张"的法案；即便完成内阁表决，后续仍需联邦议院、联邦参议院及布鲁塞尔国家援助审批，时间链条进一步压缩**

> **来源：**
> - [Germany's EEG 2027 Draft: A New Era for Renewables — Freshfields](https://www.freshfields.com/en/our-thinking/blogs/sustainability/germanys-eeg-2027-draft-a-new-era-for-renewables-102mrfg) `[2026]`
> - [EEG 2027 – Overview — Taylor Wessing](https://www.taylorwessing.com/en/insights-and-events/insights/2026/03/eeg-2027-die-geplante-novelle-des-erneuerbare-energien-gesetzes-im-ueberblick) `[2026-03]`
> - [Wohl weiter warten auf die EEG-Novelle im Kabinett — PV Magazine Deutschland](https://www.pv-magazine.de/2026/05/26/wohl-weiter-warten-auf-die-eeg-novelle-im-kabinett/) `[2026-05]`
> - [EEG 2027: Studie warnt vor 30 Jahren Amortisation — EMA Energiewelt](https://ema-energiewelt.de/wissen/eeg-2027-amortisation-30-jahre-kabinett-vertagt) `[2026-06]`
> - [Reiche auf BDEW-Kongress 2026 — PV Magazine Deutschland](https://www.pv-magazine.de/2026/06/10/reiche-auf-bdew-kongress-2026-eeg-und-netzpaket-noch-vor-der-sommerpause-ins-kabinett/) `[2026-06]`
> - [BDEW-Kongress: Reiche zeigt sich kompromissbereit — T-Online](https://www.t-online.de/finanzen/energie/id_101292472/bdew-kongress-reiche-zeigt-sich-bei-energiewende-kompromissbereit.html) `[2026-06]`
> - [Energiegesetze-Ticker: Welches Vorhaben wie weit ist — ZFK](https://www.zfk.de/politik/deutschland/energiegesetze-ticker-deutschland-reiche) `[2026-06]`
> - [Regeln zur Einspeisevergütung fehlen: Reiche kommt beim EEG nicht voran — T-Online](https://www.t-online.de/finanzen/energie/id_101318126/regeln-zur-einspeiseverguetung-fehlen-reiche-kommt-beim-eeg-nicht-voran.html) `[2026-07]`

**iMSys 智能电表部署** `[执法加速中]`

EEG 2027 草案将强制安装门槛从 7 kW 降至 2 kW，覆盖几乎所有家储用户。BNetzA 于 2026-03 下旬对 77 家未启动部署的计量点运营商启动执法程序，威胁合规罚款。

> **来源：**
> - [How is the German Smart Meter Rollout Progressing? — FfE](https://www.ffe.de/en/publications/how-is-the-german-smart-meter-rollout-progressing/) `[2026]`

### 2.4 阳台储能法规 `[阳储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **组件功率上限** | ~~模组输出最高 2000 Wp~~（已取消） | 2024-05 Solarpaket I 设定；**2026-03 VDE 取消** |
| **逆变器馈电上限** | 800W（800 VA），不变 | 2024-05 Solarpaket I 生效 |
| **Schuko 插头限制** | 使用 Schuko 连接时，模组总输出不超过 960 Wp（800W 的 120% 技术缓冲） | 2025-12 VDE 标准明确 |
| **技术标准** | DIN VDE V 0126-95 发布，规范模组功率、逆变器馈电、插头类型 | 2025-12 |
| **注册要求** | 仅需在联邦网络局（Bundesnetzagentur）市场主数据登记处注册，无需向本地电网运营商报备；含储能系统同样适用简化流程 | 2024-05 简化；2026-03 确认含储能 |
| **租户权利** | 一般允许租户安装，除非房东或住户公约明确禁止 | 2024-05 立法确认 |
| **市场规模** | 已注册超 120 万套，2024-2025 年各新增约 40 万套 | 2026 年初数据 |

**VDE-AR-N 4105:2026-03 重大更新** `[2026-03-01 生效]`

新版并网连接标准废除 Solarpaket I 所设的 2,000 Wp 模组功率上限。在 800 VA 馈电上限不变的前提下，允许阳台光伏配备更大功率组件（实测配置可达 5–10 kWp），将日间多余电力存入电池而非馈网。含储能系统的阳台光伏被正式纳入简化注册流程，无需专业电工介入，用户可自行填写专用表格完成 Marktstammdatenregister 注册。

> **来源：**
> - [New German rule allows larger plug-in PV without electrician — PV Magazine](https://www.pv-magazine.com/2026/04/08/new-german-rule-allows-larger-plug-in-pv-without-electrician/) `[2026-04]`
> - [New German allowances give further boosts for plug-in PV and storage — ESS News](https://www.ess-news.com/2026/04/10/new-german-allowances-give-further-boosts-for-plug-in-pv-and-storage/) `[2026-04]`

**VDE-AR-N 4100:2026 配套更新（计量柜/接户装置规则）** `[2026-04-01 生效]`

四大配电网技术规则同步更新的 VDE-AR-N 4100（低压接户装置技术规则）明确：阳台光伏储能的注册要求仅适用于"**固定式**"电储能系统（stationary electrical storage systems）；**移动式/便携式储能设备豁免注册要求**。该规则同时收紧计量柜（Zählerplatz）内主开关和三相计量点的布置要求。对产品定义的影响：便携储能若作为阳台光伏配套设备销售，需在产品说明和渠道物料中明确标注"非固定安装、无需注册"的属性定位，与固定式家储/阳储产品形成注册义务上的明确区隔。

> **来源：**
> - [New VDE-AR-N 4100: Changes for balcony power plants and e-car charging cables — heise online](https://www.heise.de/en/news/New-VDE-AR-N-4100-Changes-for-balcony-power-plants-and-e-car-charging-cables-9976650.html) `[2026-04]`

### 2.5 便携储能 `[移储]`

- `[2023-01 起]` 享受 0% 增值税（与家储/阳储同等待遇）
- 需符合 EU 电池法规 CE 认证和 EPR 注册要求
- 无专项补贴计划

> **来源：**
> - [Germany's Energy Storage Market — Energy Central](https://www.energycentral.com/energy-biz/post/germany-s-energy-storage-market-a-surge-driven-by-renewables-and-policy-ejF8NDW3h2vwB3l) `[2025]`
> - [Battery Storage Investment Germany 2026 — Fiegenbaum Solutions](https://www.fiegenbaum.solutions/en/blog/solar-energy-battery-storage-investments-2025) `[2026]`
> - [Germany Solar Incentives 2025: EEG, KfW & Zero VAT — SurgePV](https://www.surgepv.com/hub/solar-industry/germany) `[2025]`
> - [2025 Germany Energy Storage Market Guide — PVB](https://www.pvb.com/blog/2025-germany-energy-storage-market-guide-policies-bess-selection-industry-trends-complete-citations/) `[2025]`
> - [Balkonkraftwerk Gesetz 2026 — Anker SOLIX](https://www.ankersolix.com/de/blogs/balkonkraftwerk/balkonkraftwerk-gesetz) `[2026]`
> - [What Does the New German Plug-in PV Norm Say? — Balkon.solar](https://balkon.solar/news/2025/11/22/what-does-the-new-german-plug-in-pv-norm-say/) `[2025-11]`
> - [Balkonkraftwerk Gesetz 2026: VDE Norm — Energiemagazin](https://www.energiemagazin.com/balkonkraftwerk/vereinfachte-regeln/) `[2026]`

### 2.6 电网费政策 `[工商储]`

**AgNes 电网费改革（BNetzA，2026-05-27 初步方案）** `[制度制定中]`

BNetzA 公布新电网费体系（Allgemeine Netzentgeltsystematik Strom，AgNes）初步方案。**适用范围**：住宅低压储能 `[家储]` 和阳台光伏 `[阳储]` 明确豁免，不受影响；全体住宅用户基础电费（Grundgebühr）结构性上调（<€100/年），但与是否安装光储无关，不影响 ROI 差值；核心影响对象为大型独立 BESS `[工商储]`。

核心内容：
- ① 现有 BESS 暂不纳入电网费征缴范围（逆转 2026-01 信号）
- ② **祖父条款**：2029-08-04 前并网、且在 AgNes 最终决定前完成 FID 的项目获 **20 年**完整豁免；FID 定义：绑定订单覆盖总投资额约 50%、不可无重大财务损失撤销、加绑定并网承诺
- ③ 未来新项目适用纯容量电网费 €4,000–7,000/MW/年（BNetzA 五年滚动均值 €5,380–5,650/MW/年），**无电量计费分量**——不惩罚高频充放电，对 EMS 运营优化中性；Modo Energy 建模：最坏情况（€7k/MW/yr）仅降低 IRR 约 0.5 个百分点
- ④ **仅 2023-01-01 前并网老项目**："可避免电网费"（Vermiedene Netzentgelte）逐步退出——2026 年削减 25%、2027 年削减 50%、2028 年削减 75%
- ⑤ 动态电网费（储能）最早 2030、目标 2033；动态电网费（发电）最早 2032、目标 2035

> **进展追踪**
> - `[2026-05-27]` BNetzA 发布 AgNes 初步方案
> - `[2026 年夏]` 正式征求意见（预计）
> - `[2026 年底–2027 年初]` 框架决定终稿（预计）
> - `[2029 年起]` 新项目费率开始征收

> **来源：**
> - [Major German BESS outcomes: Grid fee exemptions remain — ESS News](https://www.ess-news.com/2026/05/28/major-german-bess-outcomes-grid-fee-exemptions-remain-higher-costs-for-prosumers/) `[2026-05]`
> - [German grid fees: Regulator unveils near-best-case for BESS — Modo Energy](https://modoenergy.com/research/germany-grid-fees-agnes-netzentgelte-bess-batteries-bnetza-update-capacity-fees-may-2026) `[2026-05]`

### 2.7 储能市场整合 `[工商储]`

**MiSpeL（Marktintegration von Speichern und Ladepunkten）** `[Festlegung 已发布]`

核心突破：共址（co-location）场景下，BESS 充入非 100% 可再生电力也不再丧失 EEG 补贴资格，允许按市场电价优化充放电策略。**适用范围**：包干方案要求光伏装机 ≥30 kW 且同一运营主体，年度补贴上限 500 kWh/kW 装机，典型住宅光储系统（5–15 kWp）不满足门槛，仅适用于 C&I 及公用级储能。

两种核算方案：
- **包干方案（Pauschaloption）**：光伏 ≥30 kW 的 C&I 系统，按标准化比例估算绿电占比，超年度上限部分按市场价结算
- **分割方案（Abgrenzungsoption）**：15 分钟级校准计量，精准核算能量流向，适合大型商业系统

认定程序完成后，电网运营商尚需 6–12 个月完成系统适配，预计实际影响在 2027 年初显现。BNetzA 已于 2026-06-30 前正式发布 Festlegung。BDEW 和 VKU 认为认定方案中的计量概念和计费逻辑"在实践中无法执行"（MaBiS-Hub 2028/2029 落地前的改造投入存在"搁置风险"）；bne 则称其"经过深思熟虑、具有前瞻性"，并呼吁各配电网运营商（DSO）立即着手实施。

> **进展追踪**
> - `[2025-10-01]` BNetzA 公开研讨会
> - `[2025-10-24]` 意见征集截止
> - `[2026-06-30]` BNetzA 须完成 EEG 电量认定程序（法定截止日）
> - `[2027 年初]` 电网运营商适配完成后实际生效（预计）
> - **`[2026-06 末]` BNetzA 按法定截止日正式发布 MiSpeL Festlegung；行业分歧：BDEW/VKU 批评计量方案不具可操作性，bne 认可方案质量并呼吁 DSO 快速落地**

> **来源：**
> - [Understanding MiSpeL: New Regulatory Framework for German Co-located Storage — GridCog](https://www.gridcog.com/blog/understanding-mispel-the-new-regulatory-framework-for-german-co-located-storage) `[2026]`
> - ['Moment of truth': 2026 regulatory agenda for large battery storage in Germany — Energy-Storage.News](https://www.energy-storage.news/moment-of-truth-the-2026-regulatory-agenda-for-large-battery-storage-in-germany/) `[2026]`
> - [MiSpeL-Entwurf: Neue Förderung für Energiespeicher und Ladepunkte — KPMG Law](https://kpmg-law.de/mispel-entwurf-neue-foerderung-fuer-energiespeicher-und-ladepunkte/) `[2026]`
> - [MiSpeL-Festlegung: "Nicht in der Praxis umsetzbar" – Verbände üben Kritik — ZFK](https://www.zfk.de/energie/strom/mispel-festlegung-bundesnetzagentur-kritik-bdew-vku) `[2026-06]`
> - [Stellungnahme zur MiSpeL-Festlegung und Appell an Verteilnetzbetreiber — bne](https://www.bne-online.de/stellungnahme-zur-mispel-festlegung-und-appell-an-verteilnetzbetreiber/) `[2026-06]`

### 2.8 市场动态 `[通用]`

**累计装机**

| 时间 | 累计装机 |
|------|---------|
| 2026-04 | 17.9 GW / 27.2 GWh |
| **2026-06 末** | **约 29.3 GWh（较 5 月末 25.4 GWh，单月新增约 3.9 GWh）** |

> **来源：**
> - [BESS Market Germany 2026: Trends & Growth Analysis — Mobility House Energy](https://mobilityhouse-energy.com/int_en/knowledge-center/article/bess-in-germany-market-overview-2026) `[2026]`
> - [Germany solar PV generation up 10% year-on-year in H1 2026 — PV Tech](https://www.pv-tech.org/germany-solar-pv-generation-increases-h1-2026/) `[2026-07]`

**季度新增**

| 季度 | 住宅光伏新增 | 储能新增 | 大型储能（>1 MWh） | 要点 |
|------|-------------|---------|-------------------|------|
| 2026 Q1 | 850 MW（同比 -21%） | 2 GWh（同比 +67%，创历史纪录） | >1 GWh（同比近四倍） | 大型储能季度新增 **7 年来首次超越住宅端**，德国储能市场进入"商业化规模化"阶段 |

> **来源：**
> - [German Solar Association confirms more storage, less solar — ESS News](https://www.ess-news.com/2026/05/04/german-solar-association-confirms-more-storage-less-solar-capacity-installed-in-q1-2026/) `[2026-05]`
> - [Drop in residential solar drives German PV down Q1 2026 — PV Tech](https://www.pv-tech.org/drop-in-residential-solar-drives-german-pv-installations-down-in-q1-2026/) `[2026]`

### 2.9 电力供应安全与容量法（StromVKG） `[工商储]`

#### 内阁已通过，进入议会程序 `[立法进行中]`

**政策正文概述：** StromVKG（原 Kraftwerksstrategie）于 **2026-05-13** 经联邦内阁（Bundeskabinett）表决通过，进入议会立法程序。目标新增 **11 GW** 备用容量，分三轮拍卖落地：① **首轮**（2026-09-01，4.5 GW）和 **次轮**（2026-12-08，4.5 GW）合计 9 GW，须满足 10 小时持续满负荷标准，实质仅适用氢气就绪型燃气机组；② **BESS 专项拍卖**（计划 2027-05-18，2 GW），取消 10 小时标准，但要求储能终端产品 **≥50% EEA 制造来源**。9 GW 气优格局实质将独立大型 BESS 排除在 2026 年两轮主体拍卖之外；中国厂商参与 2027 年 BESS 专项拍卖还面临 EEA 来源合规门槛。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-04-24 | 部级草案（Referentenentwurf）正式发布 |
| **2026-05-13** | **StromVKG 经联邦内阁（Bundeskabinett）表决通过，进入议会立法程序** |
| **2026-06（进行中）** | **联邦议院（Bundestag）完成一读；"南部加成"（Südbonus）条款——2/3 容量分配至南部——仍存争议** |
| **2026-06-19** | **联邦参议院（Bundesrat）提出修改建议（降低电网接入保证金门槛、调整财务负担结构以避免排除市政企业），联邦政府予以拒绝** |
| **2026-06-24** | **联邦议院经济委员会公开听证（KW26）；多位专家批评 Südbonus 条款可能在德国内部制造新的区域不均衡，并就容量费征收机制结构要求政府提供明确信息** |
| **计划 2026-07-10** | **联邦议院二读/三读（夏休前截止），通过后需提交 Bundesrat** |
| **2026-07-09** | **联邦议院（Bundestag）提前一天完成二读/三读表决，StromVKG 正式通过 Bundestag 立法程序** |
| **计划 2026-07-10** | **联邦参议院（Bundesrat）召开夏休前最后一次全体会议审议 StromVKG；此前 6-19 提出的保证金门槛、财务负担结构等修改诉求已被联邦政府拒绝，市政企业和中小型参与者的准入顾虑（首轮拍卖可能出现"认购不足"）仍未解决** |
| **2026-09-01（计划）** | **首轮容量拍卖（4.5 GW，10 小时满负荷标准，氢气就绪燃气机组为主）** |
| **2026-12-08（计划）** | **第二轮容量拍卖（4.5 GW，同上标准）** |
| **2027-05-18（计划）** | **BESS 专项拍卖（2 GW，取消 10 小时标准；要求储能终端产品 ≥50% EEA 制造来源）** |

> **来源：**
> - [Kraftwerksstrategie konkretisiert sich — GÖRG](https://www.goerg.de/de/aktuelles/veroeffentlichungen/24-04-2026/kraftwerksstrategie-konkretisiert-sich-der-referentenentwurf-zum-stromvkg-liegt-vor) `[2026-04]`
> - [SMC-Studie StromVKG: 11 GW Lücke — CleanThinking](https://www.cleanthinking.de/smc-studie-kraftwerksstrategie-stromvkg/) `[2026-04]`
> - [Kraftwerksstrategie passiert Bundeskabinett — PV Magazine Deutschland](https://www.pv-magazine.de/2026/05/13/kraftwerksstrategie-passiert-bundeskabinett/) `[2026-05]`
> - [German Power Plant Strategy - Draft StromVKG — Chatham Partners](https://chatham.partners/insights/german-power-plant-strategy/) `[2026]`
> - [Bundesrat will Nachbesserungen bei Gaskraftwerks-Ausschreibungen — PV Magazine Deutschland](https://www.pv-magazine.de/2026/06/19/bundesrat-will-nachbesserungen-bei-gaskraftwerks-ausschreibungen/) `[2026-06]`
> - [Experten kritisieren Südbonus im Stromversorgungsgesetz — Bundestag](https://www.bundestag.de/dokumente/textarchiv/2026/kw26-pa-wirtschaft-stromvkg-1184768) `[2026-06]`
> - [Abstimmung über Sicherung der Stromversorgung (KW28) — Bundestag](https://www.bundestag.de/dokumente/textarchiv/2026/kw28-de-versorgungssicherheit-strom-1192538) `[2026-07]`
> - [German Federal Government passes law on the provision of new capacity in the electricity market (StromVKG) — Eversheds Sutherland](https://www.eversheds-sutherland.com/en/germany/insights/german-federal-government-passes-law-on-the-provision-of-new-capacity-in-the-electricity-market) `[2026-07]`
> - [Bundesrat sieht Änderungsbedarf beim StromVKG — Deutscher Bundestag](https://www.bundestag.de/presse/hib/kurzmeldungen-1190820) `[2026-06]`

### 2.10 输电网接入竞争机制（Reifegradverfahren）`[工商储]`

#### 成熟度评级取代先到先得 `[已生效]`

**政策正文概述：** 德国四大输电系统运营商（50Hertz、Amprion、TenneT、TransnetBW）于 2026-02-05 联合宣布引入"成熟度评级程序"（Reifegradverfahren），于 **2026-04-01** 正式生效，取代沿用多年的先到先得原则（Windhundprinzip）。政策背景：截至 2025 年 Q3，四大 TSO 共收到 717 份超高压电网接入申请，合计请求容量约 270 GW，其中 545 份（211 GW）来自大型电池储能项目，已严重超出电网规划及可用接入容量。新机制将申请改为按固定周期集中收集与评审，依据可量化的成熟度标准竞争分配接入容量。

**评分标准（满分 100 分）：**

| 维度 | 权重 | 说明 |
|------|------|------|
| 场地控制 | 30% | 已取得项目用地控制权证明 |
| 技术成熟度 | 30% | 系统设计方案、设备选型、工程可行性 |
| 资金能力 | 30% | 融资到位证明、股东资信情况 |
| 协同部署加成 | 10% | 与可再生发电资产共址的附加评分 |

**申请费用与保证金：**
- 每份申请须缴纳**不可退还**申请费 **€50,000**
- 申请方可在前 6 周内申请"完整性预审"（Vollständigkeitsprüfung，可选），一旦接受须在 1 个月内缴纳 **€1,500/MW** 实现保证金（事后可抵扣建设成本贡献金 Baukostenzuschuss）

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-02-05 | 四大 TSO 联合宣布 Reifegradverfahren |
| 2026-04-01 | 第一申请周期启动（信息发布与申请受理阶段） |
| **2026-06-30** | **第一申请周期截止（24:00），申请不可补充或修改** |
| 2026-Q3（预计） | 第一周期评审结果公布 |

> **来源：**
> - [German TSOs introduce maturity-based procedure for grid-scale battery storage — ESS News](https://www.ess-news.com/2026/02/06/german-tsos-introduce-maturity-based-procedure-for-grid-scale-battery-storage-connections/) `[2026-02]`
> - [From "First Come" to "First Ready": Germany's New Maturity-Based Grid Connection Process — Herbert Smith Freehills Kramer](https://www.hsfkramer.com/notes/energy/2026-posts/from-first-come-to-first-ready-germanys-new-maturity-based-grid-connection-process-for-bess-and-large-scale-consumers) `[2026]`
> - [Germany: Maturity Evaluation Procedure for Transmission Grid Connections — Baker McKenzie](https://www.bakermckenzie.com/en/insight/publications/2026/03/germany-maturity-evaluation-procedure-for-transmission-grid-connections) `[2026-03]`
> - [How to apply for transmission grid connection under Germany's new Reifegradverfahren — Modo Energy](https://modoenergy.com/research/en/germany-bess-battery-grid-access-connection-tso-transmission-reifegrad-maturity-principle-april-2026) `[2026-04]`

### 2.11 阳台储能销售禁令判决 `[阳储]` `[已生效]`

#### LG Bochum / LG Osnabrück 裁定禁售超限储能产品

**政策正文概述：** 波鸿地方法院（LG Bochum）与奥斯纳布吕克地方法院（LG Osnabrück）于 2026-05 分别作出裁定（案号 I-12 O 29/26、18 O 117/26），禁止销售超过 960 Wp 且未配备线路过载保护的插座式阳台储能产品，首次以司法判决确认 DIN VDE V 0126-95:2025-12 标准中的 960 Wp 上限具有强制市场约束力。违规销售最高可处 **€250,000** 罚款；已购买超限产品的消费者可依法定质保（交付后两年内）要求经销商整改或更换。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025-12 | DIN VDE V 0126-95:2025-12 标准发布，设定 Schuko 插座 960 Wp 上限 |
| **2026-05-20 / 2026-05-27** | **LG Bochum、LG Osnabrück 分别裁定禁止销售超限阳台储能产品** |

> **来源：**
> - [Landgerichte stoppen Balkonkraftwerk-Speicher ohne 960-Watt-Grenze — Solarserver](https://www.solarserver.de/2026/06/22/landgerichte-verbieten-verkauf-normwidriger-balkonkraftwerk-speicher/) `[2026-06]`
> - [Gerichte untersagen Vertrieb bestimmter Steckersolar-Speicher als Plug-and-play-Lösung — PV Magazine Deutschland](https://www.pv-magazine.de/2026/06/18/gerichte-untersagen-vertrieb-bestimmter-steckersolarspeicher-als-plug-and-play-loesung/) `[2026-06]`
> - [Urteil: Balkonspeicher für mehr als 960 Watt Modulleistung dürfen ohne Leitungsüberlastschutz nicht mehr verkauft werden — Photon](https://www.photon.info/news/urteil-balkonspeicher-fuer-mehr-als-960-watt-modulleistung-duerfen-ohne-leitungsueberlastschutz-nicht-mehr-verkauft-werden/) `[2026-06]`

### 2.12 大型储能规划特权收紧（Geothermie-Beschleunigungsgesetz）`[工商储]` `[已生效]`

#### GeoBG 收紧独立式 BESS 规划特权认定标准

**政策正文概述：** 联邦议院于 **2025-12-04** 通过《地热能加速法》（Geothermie-Beschleunigungsgesetz，GeoBG），在《建筑法典》（BauGB）§35(1) 新增第 11、12 项，重新界定非建成区大型电池储能系统的"规划特权"（Privilegierung）资格：与可再生能源发电设施存在空间及功能关联的储能项目继续享有特权；**独立式项目**则须同时满足——① 距变电站（超高压/高压或高压/中压）用地边界 **200 米**以内，或距在运/已退役 **≥50 MW** 发电厂用地边界 200 米以内；② 额定功率不低于 **4 MW**。此次收紧发生在此前一轮修订刚放宽独立式储能规划特权的**数周之后**，行业认为这一政策反复增加了大型 BESS 选址的不确定性。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025 年早些时候 | 此前修订放宽独立式储能项目的规划特权资格 |
| **2025-12-04** | **联邦议院通过 GeoBG，收紧独立式 BESS 规划特权认定标准（200 米距离 + 4 MW 门槛）** |

> **来源：**
> - [Germany may curtail preferential treatment of large battery storage facilities near substations — ESS News](https://www.ess-news.com/2026/04/21/germany-may-curtail-preferential-treatment-of-large-battery-storage-facilities-near-substations/) `[2026-04]`
> - [Privileged status for battery storage systems in unzoned areas — Gleiss Lutz](https://www.gleisslutz.com/en/know-how/privileged-status-battery-storage-systems-unzoned-areas-new-nos-11-and-12-section-351-baugb-simplify-approvals-and-create-legal) `[2026]`
> - [Germany's Battery Storage Planning Privileges Face Reversal Weeks After Approval — Energy News](https://energynews.biz/germanys-battery-storage-planning-privileges-face-reversal-weeks-after-approval-as-policy-uncertainty-returns/) `[2026]`

#### PM 解读

> **[2026-07-10]**
> - **EEG 2027 内阁表决再次推迟至 7 月且无具体日期，但 2027-01-01 生效目标未变——产品准备窗口实质压缩**：从 6-24 推迟至 7 月意味着即使 7 月底过内阁、夏休后启动议会程序，Bundestag + Bundesrat 完成立法仅剩约 4 个月（9-12 月），议会仍可大幅修改条款。核心条款（取消 ≤25 kWp 馈电补偿、iMSys 门槛降至 2 kW）方向不变，但具体参数和过渡期可能在议会阶段被柔化。建议：产品路线图按"2027-01 生效"不变推进，但 ROI 计算器的馈电率参数需设计为可热更新——议会修改出台后 48 小时内完成参数切换
> - **StromVKG 一读完成但 Südbonus 争议可能影响 BESS 拍卖区域分配**：联邦议院一读中，2/3 容量分配至南部的 Südbonus 条款引发争议。若最终立法保留该条款，2027-05 的 2 GW BESS 专项拍卖中约 1.3 GW 将定向分配至南部（巴伐利亚、巴登-符腾堡），北部项目竞争空间被压缩。对有 B 端工商储业务的厂商：项目选址应优先南部电网瓶颈区域，以增加拍卖中标概率
> - **德国是家储+阳储的第一优先市场**：0% VAT + KfW 补贴 + 120 万套阳台光伏存量，政策环境在欧洲无出其右。软件本地化（德语 App、EPEX 电价集成、KfW 申请流程引导）应该是最高优先级
> - **负电价窗口规避是家储 App 的核心卖点场景**：2025-02 政策意味着用户在 EPEX 现货价为负时馈电收益为零。App 必须集成 EPEX 实时电价数据，并实现"负电价窗口自动充电、正电价窗口放电/馈电"的智能调度。这不是 AI 花活，而是直接影响用户收益的刚需功能
> - **800W 馈电上限对阳储微逆固件提出精准控制要求**：VDE V 0126-95 明确 800W 上限，意味着微逆固件必须实现精准的功率钳位（power clamping），超限馈电可能导致合规风险。App 端需要实时展示当前馈电功率和限值状态，让用户可见可信
> - **120 万套存量是阳储 App 获客的天然池子**：德国阳台光伏用户已经习惯了"装上就用"的即插即用体验。阳储产品的 App 首次配网流程必须极简（<3 分钟完成），否则直接流失。参考 Zendure 和 EcoFlow 在这块的 onboarding 设计
> - **Schuko 960 Wp 限制是产品定义的边界约束**：使用 Schuko 插头时模组不能超 960 Wp，这意味着阳储产品如果要支持 Schuko 场景，硬件功率上限已被政策锁死。App 里需要在安装引导流程中区分 Schuko vs Wieland 两种场景的功率配置
> - **EEG 2027 内阁表决悬而未决，但储能的结构性刚需已不可逆**：EEG 2027 若取消 ≤25 kWp 住宅光伏固定馈电补偿且无替代机制，新装系统 ROI 从 15.6 年拉长至 30 年以上——除非配储能规避负电价窗口并提升自消费率。6 月 24 日内阁无论是否通过，这个方向已在市场层面形成共识。App 应提前备好"光储捆绑 ROI 计算器"：用户输入系统参数后，对比"纯光伏 vs 光储组合"两条回收曲线，让 30 年 vs 10 年的对比自己说话
> - **AgNes 对家储和阳储产品线无影响，无需软件适配**：住宅低压储能和阳台光伏被 AgNes 明确豁免；全体住宅用户基础电费（Grundgebühr）虽结构性上调（<€100/年），但与是否安装光储无关——"装 vs 不装"的 ROI 差值不受影响，无需纳入收益计算器。AgNes 的核心影响对象是大型独立 BESS（纯容量费 €4–7k/MW/年 + 20 年祖父条款），属于 B 端投资测算范畴。**唯一例外**：2023-01-01 前并网的老住宅光储系统受 Vermiedene Netzentgelte 逐步退出影响（2026–2028 年累计削减 75%），若产品有此存量用户群，App 收益引擎需按年动态调整该收入项；若目标用户群不含 2023 年前存量，可完全忽略
> - **MiSpeL 仅适用于工商储（C&I）及公用级储能，与家储产品线无关**：包干方案（Pauschaloption）要求光伏装机 ≥30 kW 且同一运营主体，典型住宅光储系统（5–15 kWp）不满足准入门槛。共址 BESS 不再要求 100% 可再生电力充入才能保留 EEG 补贴，EMS 算法可以从"最大化绿电消纳"切换为"最大化市场套利"——但这一策略解绑只对 C&I 及公用级储能有意义。对同时拥有商业储能业务线的厂商，MiSpeL 意味着 B 端 EMS 需要增加"EEG 电量分割核算"模块：包干方案下监控年度 500 kWh/kW 补贴上限并自动估算绿电占比，分割方案下接入 15 分钟级校准计量数据源，满足 BNetzA 合规要求的同时最大化套利收益。家储 App 无需为 MiSpeL 做任何适配
> - **Redispatch 妥协信号落地，EEG 2027 内阁审议可期，产品路线图应立即解锁**：经济部长在 BDEW 大会公开承诺夏休前审议且明确放弃 Redispatch 条款，将 EEG 2027 内阁表决确定性从"不明朗"升级为"大概率通过"。产品规划不应继续观望——≤25 kWp 住宅光伏取消固定馈电补偿（配储豁免 50% 馈电上限）和 iMSys 门槛降至 2 kW 两条核心条款几乎必然进入最终法案。建议立即将"光储 ROI 双轨计算器（纯光伏 vs 光储对比曲线）"和"iMSys 智能电表接入兼容适配"排入 2026 Q3 开发计划，无需等待立法最终通过
> - **StromVKG 草案将独立 BESS 置于容量市场竞争劣势，B 端储能投资测算需重置收益假设**：StromVKG 11 GW 备用容量中 9 GW 明确针对氢气就绪燃气机组（满足 10 小时满负荷标准），仅 2 GW 技术中立。9 月招标若按草案落地，德国大型 BESS 无法参与主体容量补贴竞争，收益路径回归"纯套利 + AgNes 容量费"。对有 B 端工商储业务的厂商：须从投资模型中移除容量市场收益假设，向客户展示以 EPEX 套利 + AgNes 容量费为基础的 IRR 保守情景；同时关注 2 GW 技术中立容量的拍卖细则，这是 BESS 参与 StromVKG 的唯一可能窗口
> - **StromVKG 已过内阁关，BESS 唯一参与窗口（2027-05 专项拍卖）附带 ≥50% EEA 制造来源门槛，中国厂商需立即评估合规路径**：StromVKG 于 2026-05-13 经内阁通过，确定性从"草案方向"升级为"大概率立法"。BESS 的正式参与渠道是 2027-05-18 的 2 GW 技术中立专项拍卖（取消 10 小时满负荷标准），但该拍卖要求储能终端产品 **≥50% EEA 制造来源**——全球 BESS 制造高度集中于中国供应链，这一门槛对多数中国厂商构成实质准入障碍。建议三步评估：① 现有供应链能否满足 EEA 来源比例；② 欧洲合规制造路径（欧洲组装/采购欧洲电芯）可行性与成本；③ 若无法合规，将 B 端收益假设彻底切回"纯套利 + AgNes 容量费"模型。同时在议会立法完成前（预计 2026 年底），通过 BVES/Energy Storage Europe 提交意见，推动 EEA 比例要求宽松化或设置过渡期
> - **EEG 馈电补偿 2026-08-01 再降 1%，App ROI 计算器须在 7 月底前完成参数更新**：EEG 2023 内置的半年递减机制将于 8 月 1 日触发，新并网系统馈电补偿区间从当前约 5.50–12.35 ct/kWh 降至约 5.45–12.22 ct/kWh（属于定期调整，非 EEG 2027 改革范畴）。核心行动点：App 内置"光储 ROI 计算器"若将 EEG 馈电率写死，需在 7 月 31 日前更新参数，否则 8 月后新装用户的回报测算将系统性偏高，引发售后投诉。建议将 EEG 馈电率改为后端动态配置参数（每半年拉取 BNetzA/EEG 官方数据更新），彻底消除此类定期维护负担
> - **Reifegradverfahren 首轮申请 6-30 截止——德国大型 BESS 电网接入从"抢先提交"升级为"成熟度竞争"，211 GW 申请积压倒逼机制重置**：截至 2025 年 Q3，德国 TSO 已收到 211 GW 大型 BESS 电网接入申请（545 个项目），远超实际可用容量，先到先得机制已实质失效。新机制（2026-04 生效）以场地控制（30%）+ 技术成熟度（30%）+ 资金能力（30%）+ 共址加成（10%）为评分标准，用项目真实准备程度替代提交时间。对 B 端大型 BESS 业务的产品影响：① 电网接入时间线不再可预测——成熟度评审结果（Q3 公布）是实际落地节奏的决定性节点，B 端项目管理工具需将"TSO 申请状态 + 评审进度"纳入项目看板；② 共址部署（与可再生发电资产同址）获额外 10% 加分，工商储项目规划阶段应优先考虑"光 + 储共址"方案；③ €50,000 不可退还申请费意味着只有真正成熟的项目才会入场——德国大型 BESS 市场将从"圈地跑马"切换为"有序竞争"，实际开发周期更可预期但准入门槛显著提高
> - **MiSpeL Festlegung 已正式发布，但 DSO 落地分歧是 2027 年 C&I EMS 功能交付的最大风险**：BNetzA 在法定截止日（2026-06-30）前发布 MiSpeL 正式认定，Abgrenzungsoption 和 Pauschaloption 两种核算方案具有法律效力。然而 BDEW 和 VKU 批评方案计量逻辑过于复杂（"不具可操作性"），MaBiS-Hub 2028/2029 落地前的 DSO 改造投入存在"搁置风险"——即改造完成后被 MaBiS-Hub 新标准覆盖。这意味着即使 Festlegung 已发布，DSO 实际完成计量系统适配的时间可能大幅拖延。对 B 端 EMS 产品的含义：MiSpeL 核算模块应设计为"就绪即启用"架构——逻辑提前开发完成并已测试，但等 DSO 的计量数据 API 实际可用后再开关，不要依赖 DSO 实施时间表排期自己的功能交付
> - **StromVKG 二读/三读计划 7-10，立法进入倒计时——BESS 拍卖 EEA 比例要求即将成为正式法律**：Bundesrat 在 6-19 提出修改意见（降低电网接入保证金门槛）但被联邦政府拒绝；6-24 专家听证重点批评 Südbonus 可能制造区域不均衡。立法方向虽有争议，但二读/三读计划在 7-10 夏休前完成意味着 StromVKG 立法确定性极高。BESS 专项拍卖（2027-05-18，2 GW）的 ≥50% EEA 制造来源要求一旦入法，将从"可能被修改的草案条款"升格为"确定的法律合规门槛"。建议在 7-10 立法通过后 48 小时内启动供应链 EEA 比例评估——此时的合规窗口（约 10 个月）已是最后机会
> - **StromVKG 于 2026-07-09 提前一天经 Bundestag 通过，BESS 专项拍卖 EEA 门槛已入法——供应链评估窗口即刻开启**：Bundestag 于 7 月 9 日（KW28）完成二读/三读，StromVKG 正式通过议会立法程序，较计划（7-10）提前一天。BESS 专项拍卖（2027-05-18，2 GW）及其 ≥50% EEA 制造来源要求已从"草案条款"升格为已通过法律。后续须经 Bundesrat 程序。对产品线的核心行动：① 立即委托法律团队解读 StromVKG 最终文本中 EEA 来源比例的具体定义（是否包含欧洲组装）；② 在 Bundesrat 阶段通过 BVES/行业律所提交意见，聚焦过渡期设置和比例计算范围宽松化；③ 启动欧洲组装/BMS 供应商的可行性接触——距 2027-05-18 约 10 个月，是真实的最后合规窗口
> - **法院首次以判决确认 960 Wp 阳台储能上限具强制力，供应链和产品定义必须立即对齐 VDE 标准**：LG Bochum、LG Osnabrück 两地法院裁定禁售超过 960 Wp 且无线路过载保护的插座式阳台储能产品，违规最高罚款 €250,000，且已购买产品的用户可依法定质保要求整改或更换——这意味着此前处于"行业惯例"层面的 960 Wp 限制，已升级为具有强制执行力的市场准入红线。对产品端的直接行动：① 逐一核查现有及在售阳台储能 SKU 的组件功率配置和线路过载保护设计是否符合 DIN VDE V 0126-95:2025-12；② 不合规产品应立即从德国渠道下架或提供固件/硬件整改方案，避免被追溯适用法定质保义务；③ 经销商合作协议中应明确合规责任划分，防止品牌方为经销商的历史销售买单
> - **GeoBG 收紧独立式 BESS 规划特权，"变电站 200 米 + 4 MW"门槛重塑大型储能选址逻辑**：2025-12-04 通过的地热能加速法在放宽储能规划特权数周后即收紧标准，独立式项目须满足距变电站或 ≥50MW 电厂 200 米内、额定功率 ≥4MW 两个条件才能豁免常规建设规划审批。对有 B 端大型 BESS 业务的厂商：① 选址评估工具需要内置"变电站/电厂距离核算"模块，帮助项目开发前置判断是否符合规划特权资格；② 4 MW 门槛意味着更小型的独立式储能项目（<4MW）将被迫走常规规划审批程序，审批周期和不确定性显著增加，应优先规划 ≥4MW 项目以锁定特权路径；③ 政策数周内两次反复的信号是德国储能规划立法环境仍不稳定，B 端项目排期应预留额外的合规缓冲时间
> - **VDE-AR-N 4100 首次以标准形式区分"固定式"与"移动式"储能的注册义务，为便携储能划出明确的合规豁免带**：2026-04-01 生效的新规明确阳台光伏储能注册要求仅适用于固定式电储能系统，移动式/便携式设备豁免注册。这为 `[移储]` 产品线提供了清晰的合规定位依据——便携电源即便作为阳台光伏配套放电设备销售，只要不构成固定安装，即可维持"即插即用、无需注册"的产品体验，与固定式家储/阳储在渠道物料和用户告知义务上应做明确区隔（例如安装引导流程中增加"是否固定安装"的判断分支，触发不同的合规提示文案）
> - **德国储能装机 6 月单月新增约 3.9 GWh，光伏弃光 58.2% 集中于负电价时段——负电价规避已从"政策提示"变为"可量化的收益损失"，App 收益引擎应升级为可展示的对比数据**：H1 2026 德国光伏发电量同比 +10% 创新高，但弃光和负电价时段高度重合，印证配储能可直接减少弃光并提升捕获率。产品建议：App 内的"负电价规避"功能不应止步于自动调度，应增加"本月因负电价规避节省/增收金额"的可视化模块，用真实数据强化用户对储能配置价值的感知，也为渠道端提供更有说服力的销售话术素材
> - **StromVKG 进入 Bundesrat 立法收尾阶段（计划 7-10 夏休前最后表决），市政企业/中小参与者的准入顾虑未被采纳——B 端 EMS 应为首轮拍卖"认购不足"预留备选收益路径**：Bundesrat 此前提出的保证金门槛下调、财务负担结构调整诉求已被联邦政府拒绝，行业担忧 9-1 首轮拍卖可能因此出现中小型/市政参与者退场导致的认购不足。对有 B 端工商储业务的厂商：① 不应假设首轮 9 GW 气电招标必然满额成交，招标遇冷可能倒逼后续轮次（含 2027-05 的 2 GW BESS 专项拍卖）条款松动，需保持政策灵敏度；② B 端项目报价模型应同时准备"容量市场收益"和"纯套利+AgNes 容量费"两套情景，视 Bundesrat 7-10 最终结果切换基准假设
> - **StromVKG 已完成立法但 EEG 2027 仍原地踏步——两条曾经绑定的法案已实质脱钩，馈电补偿参数的不确定性比容量市场规则更持久**：Reiche 此前将 EEG 与 Netzpaket/StromVKG 捆绑表决以换取谈判筹码，但截至 7 月初（距夏休仅两周）经济部与环境部在 ≤25 kWp 馈电补偿取消方案上仍无协议，Schneider 明确拒绝任何"危及可再生能源扩张"的版本；即便本轮内阁最终过关，后续仍需完整走完联邦议院、联邦参议院及布鲁塞尔国家援助审批，EEG 现行授权 2026 年底到期的时间压力持续累积。对产品端：馈电补偿相关参数（≤25 kWp 段是否取消固定补偿、50% 馈电上限豁免条件）在 Q3-Q4 仍可能反复变动，ROI 计算器除馈电率热更新外，应额外为"过渡期空窗"场景（EEG 到期但新法未生效）设计降级展示逻辑，避免用户在立法真空期看到错误或缺失的收益预测

---

## 三、意大利

### 3.1 家庭储能补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **Ecobonus 50%/65%** | 光伏+储能系统 50% 税收抵扣（10 年分摊），适用于主要住宅；若结合建筑能效改造（需取得 APE 能效证书且能效等级提升），可提升至 **65%** | 确认延续至 2026 年底；2027 年降至 36%→30% |
| **Superbonus** | 已大幅退坡：110%→90%→70%→65%，2026 年起独立光伏不再适用 | 2025 年 65%，2026 年退出 |
| **Conto Termico 3.0** | GSE 因申请量远超预算（申请总额约 **€13 亿** vs 年度预算 **€9 亿**）于 **2026-03-03 至 2026-04-13** 暂停 PortalTermico 新申请受理，重开后追加 **40 天**申请延期以保护受暂停影响的申请人；**首次明确将光伏+储能纳入补贴**（须配套热力系统改造），最高补贴比例 **65%**；已取代 CT 2.0 成为意大利补贴强度最高的能效激励通道 | 2026-03-03 暂停，2026-04-13 重开 |
| **区域补贴** | 西西里、撒丁岛、卡拉布里亚有 EU 基金支持的区域项目 | 2025-2026 有效 |

- **申请要求**：付款必须通过可追溯的银行转账，配合官方发票和财务收据
- `[2025-11]` 裁定：储能和可再生能源项目享有 30 天许可审批窗口
- **Conto Termico 3.0 要点**：光储必须与热泵等热力系统改造捆绑才能触达 65% 最高档；已有光伏用户若同步进行热力系统升级，可申请"PV + 储能 + 热泵三合一"补贴包

> **来源（Conto Termico 3.0）：**
> - [Conto Termico 3.0: Portal Reopened April 13, 2026 — Studio RCG](https://www.studiorcg.it/en/conto-termico-3-0-portal-reopened-from-april-13-2026-for-direct-applications/) `[2026]`
> - [A full guide to the Conto Termico 3.0 — Enel](https://www.enel.it/en-us/blog/guide/guida-conto-termico) `[2026]`
> - [Conto termico 3.0: sospensione temporanea dell'invio di nuove richieste — GSE](https://www.gse.it/media/comunicati/conto-termico-3-sospensione-temporanea-dell-invio-di-nuove-richieste) `[2026-03]`
> - [Conto Termico 3.0, il Gse sospende le domande per richieste di incentivo — Sky TG24](https://tg24.sky.it/economia/2026/03/04/gse-conto-termico-3-0-sospensione-domande) `[2026-03]`

### 3.2 阳台储能政策 `[阳储]`

- `[持续有效]` 允许阳台光伏，容量上限最高 2000W
- `[至 2026 年底]` 可纳入 50% Ecobonus 税收抵扣范围
- 需关注各地方政府的具体实施细则

### 3.3 便携储能 `[移储]`

- 无专项补贴，需符合 EU CE 认证和 EPR 注册

> **来源：**
> - [Italy's 50% Tax Credit for PV & Battery Storage Extended to 2026 — Youth Power](https://www.youth-power.net/news/italys-50-tax-credit-for-pv-battery-storage-extended-to-2026/) `[2025]`
> - [Italian Ruling Secures 30-Day Permit Window — ESS News](https://www.ess-news.com/2025/11/26/italian-ruling-secures-30-day-permit-window-for-storage-and-renewables-but-size-matters/) `[2025-11]`
> - [Italy Superbonus Solar 2025-2026 — SurgePV](https://www.surgepv.com/blog/italy-superbonus-solar) `[2025]`

### 3.4 电价政策 `[通用]`

#### Decreto Bollette（电费法令）`[立法已通过]`

**政策正文概述：** 意大利政府于 2026-02-24 通过 DL no. 21/2026 "电费法令"，核心措施包括补贴气电燃气输送费及 EU ETS 排放权成本（从 2027-01-01 起生效），目的是人为压低气电边际成本以降低终端电价。行业机构警告：此举将导致太阳能捕获价下滑超 30%，同时压缩峰谷价差和电价波动，直接削弱 BESS 套利收益。EU 委员会已对 ETS 补贴机制合法性提出异议。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-02-24 | DL no. 21/2026 获批 |
| 2027-01-01 | ETS 补贴机制生效 |
| 待定 | EU 委员会对 ETS 补贴合法性审查结果 |

> **来源：**
> - [Italy's new energy provisions could boost gas use — PV Magazine](https://www.pv-magazine.com/2026/02/25/italys-new-energy-provisions-could-boost-gas-use-undermine-renewables-and-storage-competitiveness/) `[2026-02]`
> - [Italian Energy/Bills Decree DL Bollette — DLA Piper](https://www.dlapiper.com/en/insights/publications/2026/03/decreto-energia-bollette) `[2026-03]`

### 3.5 市场动态 `[通用]`

**装机概况（截至 2026 Q1）：**

| 指标 | 数值 |
|------|------|
| BESS 系统总数 | ~919,000 套 |
| 总容量 | 18.8 GWh |
| 总功率 | 7.73 GW |
| 光伏配储电化学储能 | 11.4 GWh |
| 趋势 | 住宅趋稳，C&I 与独立 BESS 增长提速 |

**长期预测（Terna）：**

| 情景 | 2030 目标 | 2035 预测 |
|------|----------|----------|
| PNIEC 目标 | 9 GW / 71 GWh | — |
| 基准情景 | — | ~134 GWh |
| 高情景 | — | ~170 GWh |

2026–2030 年被业界视为意大利储能从"光伏附件"升格为"电力基础设施"的关键五年。

**投资动态：**
- `[2026-03]` 欧洲投资银行（EIB）宣布支持意大利 **€5.07 亿**太阳能+储能项目计划，利好大型储能市场扩张

> **来源：**
> - [Italian storage market in Q1 2026 — ESS News](https://www.ess-news.com/2026/05/05/italian-storage-market-in-q1-2026-ci-and-standalone-bess-grow-residential-stabilizes/) `[2026-05]`
> - [Italy's energy storage needs could reach 170 GWh by 2035 — ESS News](https://www.ess-news.com/2026/06/12/italys-energy-storage-needs-could-reach-170-gwh-by-2035/) `[2026-06]`
> - [EIB Backs €507 Million Solar and Storage Programme in Italy — Funds for NGOs](https://news.fundsforngos.org/2026/03/18/eib-backs-e507-million-solar-and-storage-programme-in-italy/) `[2026-03]`

### 3.6 储能容量拍卖（MACSE） `[工商储]`

#### 第二轮拍卖 `[已确认]`

**政策正文概述：** Terna 确认第二轮 MACSE 储能容量拍卖于 **2026-11-24** 举行，目标容量 **16 GWh**（2029 年交付），较第一轮（2025-10-01，10 GWh）规模扩大 60%。南部及卡拉布里亚区上限升至 11.5 GWh，西西里区下限翻倍至 1 GWh。

**参与时间表：**
| 时间 | 事件 |
|------|------|
| 2025-10-01 | 第一轮拍卖完成（10 GWh） |
| **2026-07-07 至 07-27** | **第二轮申请窗口** |
| 2026-09-10 | 系统资格认证文件上传截止 |
| 2026-10-20 | 保证金及声明截止 |
| **2026-11-24** | **第二轮拍卖（16 GWh）** |

> **来源：**
> - [Italy sets November date for MACSE storage auction targeting 16 GWh — ESS News](https://www.ess-news.com/2026/06/02/italy-sets-november-date-for-macse-storage-auction-targeting-16-gwh/) `[2026-06]`
> - [Italy's MACSE 2026: bigger volumes, same rules — Modo Energy](https://modoenergy.com/research/en/italy-macse-2026-auction-bess-rules-terna) `[2026]`

#### PM 解读

> **[2026-07-01]**
> - **Ecobonus 50% 窗口期有限（至 2026 年底），市场拓展需要倒排**：Superbonus 已退出，Ecobonus 是当前唯一的重磅补贴。如果 2027 年不续期，意大利家储市场的补贴驱动力将大幅减弱。App 和 Web 端应在用户可见位置展示"补贴倒计时"和"预计节省金额"，利用紧迫感推动转化
> - **30 天审批窗口利好安装商工具链**：2025-11 裁定的 30 天许可审批窗口，意味着 B 端安装商工具需要内置项目进度跟踪（申请→审批→安装→并网），帮助安装商管理时间线。这是安装商 App 的差异化功能点
> - **阳台储能搭 Ecobonus 便车是时间窗口打法**：阳台光伏+储能可以纳入 50% Ecobonus 范围，这意味着阳储产品在意大利的定价策略可以更激进（用户实际只承担一半成本）。App 中需要内置"补贴后价格"计算器，让用户秒懂经济账
> - **银行转账+发票的合规要求影响售后链路**：Ecobonus 要求可追溯银行转账和官方发票，产品的电商流程或线下安装商流程必须确保合规凭证生成。这不是软件产品的直接需求，但影响渠道方案设计
> - **92 万套装机基数让意大利成为欧洲最大住宅储能存量市场之一，运营价值超过新增价值**：截至 2026 Q1 约 919,000 套 BESS 在运，18.8 GWh 总容量。这个规模意味着 OTA 固件升级、云端能源管理订阅、增值服务的用户池已经足够大——纯靠硬件新增销量拉收入的模式在意大利应该升级为"硬件 + 软件订阅 + 服务"的复合模型，存量用户的 ARPU 提升比新增装机更值得优先关注
> - **住宅端趋稳、C&I 端加速，意大利软件需求正在分层**：2026 Q1 数据显示住宅市场增速趋缓，商工业储能快速扩张，Terna 的 2035 年预测（134–170 GWh）中大量增量来自大型 BESS。对产品线的含义：不能只做面向消费者的手机 App，需要同步规划 B 端能源管理 Web 平台；170 GWh 的长期市场体量，完全支撑意大利市场的独立 B 端软件投入
> - **Conto Termico 3.0 是 Superbonus 退出后最重要的政策补位，但光储必须与热泵捆绑才能触达 65% 最高补贴档**：CT 3.0 的 65% 上限要求同期进行热力系统（热泵）改造，纯光储安装无法触达最高档补贴（只能享受更低档次）。对产品策略的影响：意大利市场应优先打通与本地热泵品牌（Daikin、Bosch、Vaillant 意大利经销商网络）的捆绑方案，而非单独推储能；App 端需支持热泵联动控制（或至少与主流热泵品牌 API 集成），让安装商能向客户提供"光伏+储能+热泵三合一"捆绑报价及 GSE 补贴测算——这是意大利市场 2026 年最有竞争力的销售话术
> - **MACSE 第二轮拍卖（2026-11-24，16 GWh）是意大利工商储最确定的 2026 年政策机遇，7 月 7 日申请窗口不可错过**：16 GWh 较首轮扩大 60%，15 年期长期合约是意大利大型 BESS 最稳健的收益来源，已有 Octopus/ZE Energy 等机构通过首轮 MACSE 合约锁定了 Sessa Aurunca 895 MWh 项目。对有工商储产品线的厂商：7 月 7 日为申请窗口开放日，须在 9 月 10 日前完成系统资格认证文件上传——认证流程不可跳过，立即启动是参与本轮拍卖的唯一路径
> - **Conto Termico 3.0 申请量远超预算（€13 亿 vs €9 亿）导致portal暂停 40 天，印证光储+热泵捆绑需求旺盛，但也暴露"先到先得"审批的排队风险**：GSE 于 2026-03-03 至 04-13 暂停新申请受理，说明市场对"光伏+储能+热泵"捆绑补贴的真实需求远超预算规划。对渠道和产品策略的含义：① 安装商 B 端工具应内置"补贴预算实时消耗进度"提示，帮助安装商判断当前申请的资金池剩余空间，避免客户因预算耗尽而无法获批产生纠纷；② 重开后 40 天的补偿性延期表明政府认可"先到先得"机制对被暂停期用户不公平，未来同类补贴计划设计时（尤其是与安装商合作推广节奏）应考虑"申请量预警"而非等到暂停才告知用户；③ 该案例可作为向用户解释"为什么要尽快申请"的真实依据，提升安装商销售话术的说服力

---

## 四、法国

### 4.1 自消费补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **Prime à l'Autoconsommation** | 自消费资本补贴，<3 kWp 系统最高约 €1,900/kWp（5 年分期发放） | 持续有效 |
| **Obligation d'Achat (OA)** | 馈电补贴，<3 kWp 全额馈电最高 €0.2349/kWh | 持续有效 |
| **TVA 减免** | <3 kWp 安装在既有住宅上，增值税降至 10%（标准 20%） | 持续有效 |

- `[截至 2026-06]` **无专门针对家庭储能的国家级补贴**，主要通过光伏自消费补贴间接支持储能配套
- MaPrimeRénov 覆盖热力改造和采暖系统，**不直接覆盖光伏和储能**

### 4.2 电网费率改革 `[家储]`

- `[2026-08 生效]` 储能项目可选择新的"注入-提取"（injection–withdrawal）电价方案
- 抽取区域：冬季高峰时段（8-12 点、17-21 点）放电获得奖励
- 注入区域：夏季午间充电获得奖励
- **影响**：为家储的分时电价优化提供了政策基础

### 4.3 集体自消费 `[家储]` `[阳储]`

- `[持续有效]` 允许同一低压网络内的建筑群共享光伏发电，减免共享部分的电网费用
- 适用于公寓楼和小型商业集群
- `[2026-05]` 集体自消费模式遇到监管审批瓶颈
- `[2026-06-26]` 法国政府发布法令，修订集体自消费分摊规则：确立"自消费最大化"原则，取消基于实际用电量和市场价格的**事后（ex post）分摊系数调整**机制；行业观点认为，随着光伏公共支持力度下降、馈网限制趋严，储能电池正从"锦上添花"升级为提升集体自消费项目经济性的关键杠杆——白天蓄电、晚间放电可显著提高自消费比例
- `[2026-03-30]` 法国最高行政法院（Conseil d'État）裁定：此前税务机关对 <1 MW 集体自消费项目消费税（accise）0 欧元豁免附加的适用条件缺乏法律依据，判决豁免适用于所有符合资质的集体自消费项目
- `[2026 Q1]` 集体自消费项目数量同比增长 **20%**，参与者数量增速更快于项目数量，行业预测法国将成为欧洲增长最快的集体自消费市场（至 2030 年）

> **来源（Conseil d'État 裁定 + Q1 数据）：**
> - [Autoconsommation collective : l'accise à 0 euro confirmée pour les opérations inférieures à 1 MW — PV Magazine France](https://www.pv-magazine.fr/2026/03/31/autoconsommation-collective-laccise-a-0-euro-confirmee-pour-les-operations-inferieures-a-1-mw/) `[2026-03]`
> - [Autoconsommation collective : 320 opérations au T1 2026 — Les Énergies Renouvelables](https://www.les-energies-renouvelables.eu/320-nouvelles-operations-autoconsommation-collective-au-premier-trimestre-2026/) `[2026-Q1]`

> **来源（2026-06-26 法令）：**
> - [L'intérêt des batteries en renfort de l'autoconsommation collective — PV Magazine France](https://www.pv-magazine.fr/2026/06/02/les-batteries-en-renfort-de-lautoconsommation-collective/) `[2026-06]`
> - [Autoconsommation collective : les règles de répartition modifiées par décret — Actu-Environnement](https://www.actu-environnement.com/ae/news/decret-autoconsommation-collective-repartition-energie-48232.php4) `[2026-06]`

### 4.4 阳台储能政策 `[阳储]`

- `[持续有效]` 允许阳台光伏，容量上限最高 2000W
- `[2025]` 简化了小型光伏的审批流程
- 提供安装税收抵免
- 储能审批涉及电网影响评估、正式检查和审批，通常需数月，进度慢于德国和荷兰

> **来源：**
> - [France EDF Feed-in Tariffs 2026 — SurgePV](https://www.surgepv.com/blog/france-feed-in-tariffs) `[2026]`
> - [Solar Self-Consumption Rules in Europe — SurgePV](https://www.surgepv.com/blog/solar-self-consumption-rules-europe) `[2026]`
> - [France Revises Grid Tariffs for Battery Storage — PV Magazine](https://www.pv-magazine.com/2025/10/10/france-revises-grid-tariffs-to-spur-smarter-battery-storage-use/) `[2025-10]`
> - [France Grid Tariff Reforms for Energy Storage — Energy Storage News](https://www.energy-storage.news/france-introduces-grid-tariff-reforms-for-energy-storage/) `[2025-10]`
> - [France Collective Self-Consumption Hits Regulatory Wall — PV Magazine](https://www.pv-magazine.com/2026/05/14/frances-collective-solar-self-consumption-model-hits-regulatory-wall/) `[2026-05]`

#### PM 解读

> **[2026-07-05]**
> - **法国是"政策空白型"市场，短期优先级低于德国和意大利**：无专项储能补贴意味着用户的购买决策完全靠经济性自驱（自消费省电 vs 系统成本）。App 中的"投资回报计算器"在法国市场比任何地方都更关键——用户需要被说服，而不是被补贴推动
> - **2026-08 电网费率改革是战略转折点**：injection-withdrawal 电价方案落地后，家储 App 必须支持"冬季峰时放电、夏季午间充电"的分时策略。这和德国的负电价规避、英国的 SEG 分时售电本质上是同一个软件能力——**动态电价响应引擎**。如果产品在德国已经做了 EPEX 集成，法国市场的适配成本会大幅降低
> - **集体自消费是差异化方向但风险高**：公寓楼共享光伏场景对家储和阳储都有需求，但 2026-05 已遇到监管瓶颈。短期不建议重仓这个方向，但可以在 App 架构上预留"多用户共享能源管理"的扩展接口
> - **阳储审批慢是市场进入的实际障碍**：法国储能审批需数月（vs 德国即插即用），这意味着阳储产品在法国的渠道策略不能照搬德国的"用户自装"模式，可能需要更多依赖安装商渠道
> - **2026-06-26 法令取消事后分摊系数调整，B 端集体自消费 EMS 需要从"事后核算"转向"事前优化"架构**：新规确立"自消费最大化"原则并取消基于实际用电和市场价格的事后分摊调整，意味着分摊策略必须在电力生产/消费发生前就确定，无法再依赖月末/年末的回溯校正。对面向公寓楼、社会住房等集体自消费场景的 B 端能源管理平台：储能调度算法需要承担起"事前预测 + 实时分摊执行"的双重职责，而非过去"先记录用电、后调整分摊系数"的简化模式；这也是储能在集体自消费项目中从"可选配件"转变为"分摊优化刚需组件"的政策信号，可作为向社会住房运营商推销 B 端 EMS + 储能捆绑方案的新论据
> - **Conseil d'État 裁定消除税务合规不确定性 + Q1 项目数 +20%，集体自消费从"风险方向"转为"可加速投入的确定性赛道"**：此前 2026-05 提及的"监管审批瓶颈"中，税务处理的不确定性是主要顾虑之一——税务机关此前对 <1 MW 项目 0 欧元消费税豁免附加了法律未授权的限制条件，Conseil d'État 已明确裁定该限制违法，所有合规项目均适用豁免。叠加 Q1 项目数量 +20%、参与者增速更快的市场数据，此前"短期不建议重仓"的判断需要上调优先级：① B 端 EMS 的"多用户共享能源管理"扩展接口（此前列为预留项）应提前排入 2026 H2 开发计划，而非继续观望；② 税务合规不确定性消除后，安装商向公寓楼/社会住房推荐"集体自消费+储能"方案时的销售阻力显著降低，渠道物料可以直接引用 Conseil d'État 裁定作为合规背书

---

## 五、西班牙

### 5.1 自消费框架 `[家储]` `[阳储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **RD 244/2019** | 自消费基础框架，compensación simplificada 机制：按 PVPC 现货价格月度结算余电，不跨月滚存 | 持续有效，截至 2026 无重大修订 |
| **PVPC 余电价格** | 平均 €0.04–€0.12/kWh（随小时和季节波动） | 2025-2026 |
| **集体自消费扩展** | 共享半径扩大至 5 km（≤5 MW 项目适用），新增"自消费管理人"（gestor de autoconsumo）角色，代表参与消费者统一对接配电商/售电商 | 2025 提出；**2026-03-20 经 RDL 7/2026 正式立法** |
| **双重模式兼容** `[新增]` | 允许消费者同时参与"无余电个体自消费"与"电网关联式集体自消费"两种模式，此前二者互斥 | **2026-03-20（RDL 7/2026）** |

**RDL 7/2026 背景：** 该法令是西班牙政府应对中东（伊朗/霍尔木兹海峡）能源危机的"综合应对计划"（Plan Integral de Respuesta a la Crisis en Oriente Medio）组成部分，与 EU 层面 AccelerateEU 应急工具箱（见 1.9）同属危机响应政策序列，核心目标是加速自消费和分布式能源社区落地以降低对外部能源依赖。

### 5.2 补贴政策 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **IDAE Next Generation EU** | 覆盖 15-40% 系统成本（住宅和 SME） | 持续有效 |
| **制造业激励** | €7.5 亿+可再生能源和储能制造激励（首轮） | 2025 |
| **大型储能** | €8.4 亿 ERDF 资金，支持 133 个项目共 2.4 GW / 10 GWh | 2025-12 |

- 住宅级储能补贴细则需跟踪各自治区（Comunidad Autónoma）政策

### 5.3 阳台储能政策 `[阳储]`

- `[持续有效]` 允许阳台光伏系统
- 余电补偿制度（非 1:1 净计量，按 PVPC 现货价）
- 各自治区政策差异较大

> **来源：**
> - [Royal Decree 244/2019 Spain: Complete Guide — SurgePV](https://www.surgepv.com/blog/spain-net-metering-benefits) `[2026]`
> - [Solar Panels Spain 2026: IDAE Grants — SurgePV](https://www.surgepv.com/blog/residential-solar-adoption-spain) `[2026]`
> - [Spain Allocates €840M for Storage — Energy Storage News](https://www.energy-storage.news/spain-allocates-e840-million-funds-for-storage-projects-passes-grid-resilience-decree/) `[2025]`
> - [Spain Awards 133 Storage Projects — PV Magazine](https://www.pv-magazine.com/2025/12/01/spain-awards-133-energy-storage-projects-totaling-2-4-gw-and-10-gwh/) `[2025-12]`
> - [Real Decreto-ley 7/2026 y autoconsumo: qué cambia en 2026 — Araoz & Rueda](https://www.araozyrueda.com/autoconsumo-compartido-espana/) `[2026-03]`
> - [BOE-A-2026-6544: Real Decreto-ley 7/2026, de 20 de marzo, Plan Integral de Respuesta a la Crisis en Oriente Medio — BOE](https://www.boe.es/buscar/act.php?id=BOE-A-2026-6544) `[2026-03]`
> - [Ampliado hasta los 5 kilómetros el límite al autoconsumo — PV Magazine España](https://www.pv-magazine.es/2026/03/23/ampliado-hasta-los-5-kilometros-el-limite-al-autoconsumo-una-las-medidas-para-mitigar-el-impacto-de-la-guerra-en-oriente-proximo/) `[2026-03]`

### 5.4 市场动态 `[通用]`

**管线与装机（截至 2026 Q1）：**

| 指标 | 数值 | 同比变化 |
|------|------|---------|
| 公众咨询阶段储能项目 | 96 个 / 2,121.5 MW | — |
| 其中 BESS | 2,098.2 MW（占比 98.9%） | **+464%** |
| 已并网储能装机 | 193 MW（截至 2026-04） | **+589%**（2025-04: 28 MW） |

大型独立 BESS 项目和光储协同部署是增长主体，住宅补贴政策层面无重大更新。

> **来源：**
> - [Battery energy storage project pipeline in Spain surges 464% year-on-year — ESS News](https://www.ess-news.com/2026/04/24/battery-energy-storage-project-pipeline-in-spain-surges-464-year-on-year/) `[2026-04]`

### 5.5 容量机制 `[工商储]`

#### EU 批准西班牙 €90 亿容量机制 `[已生效]`

**政策正文概述：** 欧盟委员会于 **2026-05-29** 依据 EU 国家援助规则批准西班牙电力供应安全 **€90 亿容量机制**，认定其符合 Clean Industrial Deal State Aid Framework。该机制由西班牙系统运营商 Red Eléctrica de España（REE）负责实施，从 **2026 年 5 月起运行 10 年**，年度预算约 **€9 亿**（具体金额视拍卖结果调整）。适用主体涵盖发电资产、储能系统和需求侧响应，参与者将通过容量拍卖获得"在系统压力或电力短缺时段维持可用性"的补偿。西班牙国家可靠性标准定义为：每年最大可接受断电小时数（maximum acceptable number of load-loss hours）。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-05-29 | 欧盟委员会批准西班牙 €90 亿容量机制（国家援助审查通过，符合 Clean Industrial Deal 框架） |
| **2026-05 起** | **机制正式启动，REE 开始运行容量拍卖程序，10 年周期** |

> **来源：**
> - [EU approves Spain's €9 billion capacity market for generation, demand response and energy storage — Energy-Storage.News](https://www.energy-storage.news/eu-approves-spain-euro-9-billion-capacity-market-generation-demand-response-energy-storage/) `[2026-06]`
> - [EU approves capacity market for Spain — ESS News](https://www.ess-news.com/2026/06/01/eu-approves-capacity-market-for-spain/) `[2026-06]`
> - [Commission approves €9 billion Spanish capacity mechanism for security of electricity supply — European Commission](https://ec.europa.eu/commission/presscorner/detail/en/ip_26_1163) `[2026-05]`

#### PM 解读

> **[2026-07-04]**
> - **PVPC 现货价波动大（€0.04-0.12/kWh），分时电价优化能力是西班牙市场的核心软件差异化**：余电按小时现货价结算且不跨月，用户的实际收益高度依赖"什么时候充、什么时候放"。App 必须集成 PVPC 实时电价数据，并提供可视化的"最优充放电时间窗口"建议。Zendure 在这块已经有 AI 驱动的分时优化，是对标方向
> - **集体自消费 5 km 扩展打开社区级储能管理场景**：5 km 共享半径 + "自消费管理人"角色，意味着未来可能出现"一个管理人管理多户储能"的 B 端场景。App 架构需要考虑"多设备多用户"的管理模式。短期不急，但值得在产品路线图上标记
> - **各自治区政策碎片化增加本地化复杂度**：住宅储能补贴由各自治区管理，不是联邦统一标准。App 中的"补贴查询"功能如果做西班牙市场，需要按地区适配——用户输入邮编后展示对应区域的补贴信息
> - **BESS 管线+464%、装机+589% 说明西班牙大型储能市场正在爆发，但住宅端受益有限**：Q1 2026 的数据爆发来自大型独立 BESS 和光储捆绑的商业项目，不是住宅补贴政策驱动。对家储产品线的含义：西班牙整体政策环境向好、市场生态趋于成熟，可以把西班牙纳入"2027-2028 进入"的候补市场，但当前不应把住宅端管线爆发误读为 C 端消费市场的信号
> - **EU 批准 €90 亿容量机制是西班牙工商储 B 端的重要政策锚点，但住宅端无直接受益**：容量机制覆盖发电、储能和需求侧响应，BESS 通过竞价获得可用性补偿。10 年周期 + €9 亿/年的体量为大型独立 BESS 项目提供了稳定收益预期，是西班牙 B 端工商储市场爆发的政策底座（与管线+464% 的市场数据相互印证）。对产品策略的含义：西班牙大型 BESS 的收益路径已从"纯套利"升级为"容量补偿 + 套利"双轨，B 端 EMS 平台需要增加"容量机制合规运营"模块（确保设备在系统压力时段可用并可被调用），并在 B 端报价场景中将容量机制收益纳入 IRR 测算——这会显著缩短西班牙 BESS 项目的投资回收期
> - **RDL 7/2026"双重模式兼容"打开家储+集体自消费叠加的新产品场景，App 需要支持单用户多份额账本**：此前个体自消费（无余电）与电网关联式集体自消费互斥，新规允许同一消费者同时参与两种模式——例如自家屋顶光伏优先自用，不足部分再从楼宇集体自消费池按份额补充。这是西班牙特有的场景，此前 App 的账户模型假设"一户一个自消费主体"，现在需要支持"个体账本 + 集体份额账本"并行核算，收益/账单页面需要分别列示两笔来源，避免用户混淆。建议放在 2027 西班牙市场深化阶段的产品需求清单中，短期可先在后端数据模型层面预留字段，避免后续大改

---

## 六、荷兰

### 6.1 储能补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **电池储能专项补贴** | €1 亿，目标部署 160–330 MW 储能容量 | 2025-01 起至 2034 年 |
| **电网优惠** | TenneT 提议对电池等灵活性资源降低输电费率，最高降 65% | 2024 年提议 |

- `[2025]` 属于"气候基金多年期计划 2025"的一部分

### 6.2 净计量退坡 `[家储]` `[阳储]`

| 时间节点 | 内容 |
|---------|------|
| `至 2026-12` | 净计量（Saldering）方案允许余电抵扣未来电费 |
| `2027-01-01 生效` | **终止住宅净计量**，转向自消费模式 |

- **影响**：`[阳储]` 净计量终止将显著推动阳台储能需求 — 自消费经济性倒逼配储

**政策机制解读：**

荷兰净计量（Saldering）的本质是"年度电量对冲"——光伏余电反送电网后可 **1:1 抵扣** 未来购电量，电网等效于免费虚拟电池。终止原因在于该机制对电网公司和非光伏用户不公平：光伏用户以低峰价值的余电换取等值的高峰电力，电网承担调度和输送成本却无法通过电价差回收，在荷兰光伏高渗透率下财务失衡已不可持续。

**终止后的用户影响：**

转向自消费模式后，余电不再 1:1 抵扣，反送电网收益将大幅低于购电价格。用户的经济最优策略从"尽量多发、反正能抵"变为"**发了就地消纳，避免反送**"。这直接倒逼配储需求——用户需要电池将白天余电存住、晚高峰自用，而非低价送出再高价买回。

**对软件产品的意义：**

净计量终止本质上改变了用户核心价值主张：光伏 ROI 从"卖电"转向"省电"。App 侧的**自消费率实时可视化**和**智能充放策略**（白天充、晚高峰放）从 nice-to-have 升级为核心功能。

### 6.3 阳台储能政策 `[阳储]`

- `[持续有效]` 允许即插即用光伏，无需正式注册
- 净计量退坡后，阳台光伏+储能组合的经济性将大幅提升

> **来源：**
> - [Netherlands Dedicates €100 Million to Battery Storage — ACE Battery](https://www.acebattery.com/blogs/netherlands-dedicates-100-million-to-subsidize-battery-storage) `[2024]`
> - [Netherlands Allocates €100M for Battery Storage — PV Magazine](https://www.pv-magazine.com/2024/04/18/netherlands-allocates-e100-million-for-battery-storage-subsidies/) `[2024-04]`
> - [Subsidies for Battery Storage — Intercel](https://intercel.eu/knowledge-insights/subsidies-for-battery-storage/) `[2024]`

### 6.4 市场动态 `[通用]`

**净计量终止立法进展：** `[已立法]`

荷兰议会已正式批准 Saldering 终止方案，2027-01-01 生效为不可逆的立法结果。随着截止日期临近，多家国际家储品牌（如 Jackery SolarVault 3 系列）于 2026-Q1 进入荷兰市场。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2024-11 | 荷兰议会正式批准终止净计量 |
| 2026-Q1 | 国际家储品牌密集进入荷兰市场 |
| **2027-01-01** | **净计量正式终止，转向自消费模式** |
| **2027-06（预计）** | **荷兰政府出台国家灵活性与储能综合政策议程**（integral policy agenda for energy storage），设定国家储能部署目标 |

**住宅储能市场数据：**

| 指标 | 数值 |
|------|------|
| 2025 年新增住宅光伏 | 164,000 套（较 2023 峰值 **-72%**） |
| 家用储能（Thuisbatterij）增速 | 同比 **+140%** |
| 2026 年住宅储能新增预计 | **1.7 GWh** |
| 十年末总储能容量预测 | **36.8 GWh**（住宅 14.6 + C&I 12.1 + 大型 10.1 GWh） |

净计量终止倒逼用户提前配储，成为市场增长的核心驱动力；光伏新增骤降与储能爆发形成"剪刀差"。

> **来源：**
> - [Dutch parliament approves end of net metering in 2027 — PV Magazine](https://www.pv-magazine.com/2024/11/15/dutch-parliament-approves-end-of-net-metering-in-2027/) `[2024-11]`
> - [With Dutch net metering at an end, SolarVault 3 lands in Netherlands — NL Times](https://nltimes.nl/2026/04/09/dutch-net-metering-end-solarvault-3-energy-solutions-land-netherlands) `[2026-04]`
> - [Dutch home batteries rise as solar panel additions plummet — IOplus](https://ioplus.nl/en/posts/dutch-home-batteries-rise-as-solar-panel-additions-plummet) `[2026]`
> - [Residential installations lead Dutch storage boom — ESS News](https://www.ess-news.com/2025/11/24/residential-installations-lead-dutch-storage-boom/) `[2025-11]`
> - [5 answers shaping Dutch energy storage in 2026 — Solarplaza](https://www.solarplaza.com/resource/13513/article-5-answers-shaping-dutch-energy-storage-2026/) `[2026]`

#### PM 解读

> **[2026-06-21]**
> - **爆发已经在 2026 发生，不要等 2027——光伏渠道失效，必须建立独立储能渠道**：住宅储能 2025 年同比增长 140%，2026 年预计新增 1.7 GWh；与此同时，住宅新增光伏同比跌 72%，"光伏安装商顺带推储能"的渠道模式在荷兰已经失效。进入荷兰市场必须依靠独立的储能安装商合作网络或 D2C 渠道。2026 年下半年是最大的销售窗口，错过后 2027 年的竞争强度将明显更高
> - **"即插即用、无需注册"是荷兰阳储的体验底线**：荷兰允许即插即用光伏且无需注册，这意味着用户预期是"买来插上就能用"。阳储 App 的首次配网和激活流程如果超过 5 分钟或需要专业安装商介入，就违背了市场心智。Anker SOLIX Solarbank 在这块的即插即用体验是对标标杆
> - **€1 亿储能补贴聚焦中大型系统，家储可能受益有限**：需要跟踪 SPULA 补贴的实际分配情况，判断住宅级储能的实际受惠比例
> - **36.8 GWh 十年预测支撑荷兰市场的长期本地化投入**：荷兰到本十年末预测总储能容量 36.8 GWh（住宅 14.6 + C&I 12.1 + 大型 10.1 GWh），是欧洲住宅储能密度最高的市场之一。荷兰语 App 本地化、本地电力零售商电价 API（Eneco、Vattenfall、Vattenfall 等）接入、自消费率实时可视化——这些投入在 36.8 GWh 市场规模下具有清晰 ROI
> - **荷兰 2027-06 国家储能目标是 B 端大型 BESS 的政策锚点信号**：荷兰政府预计在 2027 年 6 月出台国家灵活性与储能综合政策议程，设定量化储能部署目标——这是继净计量终止（2027-01）之后第二个对储能行业具有信号意义的政策节点。对产品策略影响：目标确定前，荷兰大型 BESS 投资决策处于"等待政策锚点"阶段；目标公布后，将为 C&I 和独立 BESS 项目开发商提供长期确定性。现阶段建议跟踪目标的具体 GW/GWh 量化值，以判断荷兰是否值得为 B 端储能管理平台做专项本地化投入

---

## 七、英国

### 7.1 税收与补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **0% 增值税** | 储能硬件及安装服务零税率（与光伏、热泵同等） | 2024 起，确认延续至 2027-03 |
| **ECO4** | 能源公司义务计划（£4B），低收入家庭可获光伏+储能安装资助。ECO5 已取消，不再延续 ECO 框架 | 运行至 2026-12-31 |
| **Warm Homes Plan** | £150 亿计划（WH:LG 低收入补贴 + WH:SHF £7.54 亿社会住房 + £20 亿零息贷款），含光伏、电池（£2,500 补贴）、热泵。低收入家庭全额覆盖 | 2026-01 发布，目标 2030 覆盖 500 万户 |
| **苏格兰免息贷款** | 最高 £6,000，叠加 0% VAT | 持续有效 |

### 7.2 售电机制 `[家储]`

- **Smart Export Guarantee (SEG)**：余电售回电网
- 配合智能电表和分时 SEG 电价，可在高价窗口放电，最高可达 50p/kWh
- **影响**：储能从自消费工具升级为售电收入工具

### 7.3 VPP 与辅助服务参与 `[家储]`

- 家储通过 VPP 聚合参与频率响应、需求侧响应等辅助服务市场
- 容量市场拍卖详情见 → **7.6 电力市场参与（容量市场 & LDES）**

### 7.4 阳台/便携储能 `[阳储]` `[移储]`

- 英国无针对阳台储能的专项法规框架
- 0% VAT 适用于所有家庭储能设备（含阳台储能产品）
- 便携储能无专项政策

> **来源：**
> - [UK Solar Incentives 2025: SEG, Zero VAT & Grants — SurgePV](https://www.surgepv.com/hub/solar-industry/uk) `[2025]`
> - [EU and UK Energy Storage Regulation 2026 — Morgan Lewis](https://www.morganlewis.com/pubs/2026/03/eu-and-uk-energy-storage-regulation-in-2026-and-beyond) `[2026-03]`
> - [Battery Storage 576 MW in UK Capacity Market — PV Magazine](https://www.pv-magazine.com/2026/03/06/battery-storage-awarded-576-mw-in-uk-top-up-capacity-market-auction/) `[2026-03]`
> - [Record-breaking 2025 for UK Battery Storage — Energy Storage News](https://www.energy-storage.news/another-record-breaking-year-for-uk-battery-storage-as-4gwh-comes-online/) `[2025]`

**详细分析见 → [英国 Warm Homes Plan & Social Housing 专题分析](uk_warm_homes_plan_analysis.md)**（含 ECO4 终局、WHP 三层资金结构、Social Housing 批量部署、安装商工具规划、EPC Smart Readiness 战略窗口）

### 7.5 安装标准 `[家储]`

#### BS 7671:2018 Amendment 4 `[已发布，2026-10-15 强制]`

**政策正文概述：** 英国电气布线法规 BS 7671:2018 第四号修订案（2026-04-15 发布）正式引入独立的"固定式蓄电池"专章，涵盖家用及商用储能系统。

**核心要求：**
- **明确禁止**在阁楼（loft）或逃生路线（楼梯、走廊等）安装电池，以降低热失控扩散风险
- 安装位置须具备充足通风、可维护性和紧急隔离点（safe isolation point）
- **2026-10-15** 起所有新建住宅电池安装须符合 Amendment 4 要求
- 违规安装将影响保险理赔及房屋售出前的 EPC 认证

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-04-15 | Amendment 4 正式发布 |
| **2026-10-15** | **强制适用于所有新建住宅电池安装** |

> **来源：**
> - [New rules ban home batteries from lofts in UK homes — Homebuilding](https://www.homebuilding.co.uk/eco-homes/energy/home-battery-systems-banned-from-lofts-under-new-wiring-rules) `[2026]`
> - [Home Battery Installation Rules UK 2026 — Habo Energy](https://haboenergy.co.uk/home-battery-installation-rules-uk) `[2026]`

### 7.6 电力市场参与（容量市场 & LDES） `[工商储]`

#### 容量市场拍卖 `[已完成]`

2026 年英国容量市场已为储能锁定超 **1.8 GW** 合同容量：

| 拍卖类型 | 交付年 | BESS 获批容量 | 清算价格 |
|---------|--------|-------------|---------|
| T-1 | 2026/27 | 576 MW | — |
| T-4 | 2029/30 | **1.22 GW**（去额定） | £27.10/kW/年（2022 年以来最低） |

在建项目占 T-4 获批容量的绝大多数。

#### LDES Cap and Floor 机制 `[制度制定中]`

Ofgem 的 LDES Cap and Floor 机制为长时储能（抽水蓄能、压缩空气等）提供收益上下限保障，降低长期资本风险。Window 1 共 77 个项目（总计 28.7 GW）通过资格审查后，Ofgem 于 **2026-06-26** 发布"拟授权"（minded-to）决定，从 73 个仍在列的合格项目中遴选 **16 个项目（合计 7.6 GW / 136.9 GWh）**进入授权候选名单，同步开启公众征询（截止 **2026-08-07**）。技术分布：锂离子 BESS 和抽水蓄能为主，含压缩空气储能（CAES）和全钒液流/锌混合阴极新兴路线，时长覆盖 8–22 小时。正式合同授予预计 2026 年夏，届时各项目 Cap/Floor 初始收益上下限将被确定。LDES 激励与容量市场互补，构建多时长储能政策矩阵。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025-09 | Window 1 资格审查结果：77 个项目（28.7 GW）通过 |
| **2026-06-26** | **Ofgem 发布 minded-to 决定：16 个项目（7.6 GW / 136.9 GWh）入选候选名单，公众征询开启** |
| **2026-08-07** | **征询截止** |
| **2026 年夏（预计）** | **正式合同授予，Cap & Floor 初始收益上下限确定** |

> **来源：**
> - [Batteries awarded 1.22 GW in UK capacity market auction for 2029 delivery — ESS News](https://www.ess-news.com/2026/03/11/batteries-awarded-1-22-gw-in-uk-capacity-market-auction-for-2029-delivery/) `[2026-03]`
> - [EU and UK Energy Storage Regulation 2026 — Morgan Lewis](https://www.morganlewis.com/pubs/2026/03/eu-and-uk-energy-storage-regulation-in-2026-and-beyond) `[2026-03]`
> - [LDES Cap & Floor Window 1 eligibility outcome — Ofgem](https://www.ofgem.gov.uk/decision/long-duration-electricity-storage-cap-and-floor-application-window-1) `[2025-09]`
> - [UK's Ofgem goes big on LDES cap-and-floor window 1; 18-hour lithium-ion among winners — Energy-Storage.News](https://www.energy-storage.news/uks-ofgem-goes-big-on-ldes-cap-and-floor-window-1-18-hour-lithium-ion-among-winners/) `[2026-06]`
> - [Long duration electricity storage window 1: minded-to decisions — Ofgem](https://www.ofgem.gov.uk/consultation/long-duration-electricity-storage-window-1-minded-decisions) `[2026-06]`

### 7.7 社区储能 `[通用]`

#### 社区电池征询 `[政策征询中]`

**政策正文概述：** DESNZ（英国能源安全与净零部）于 2026-06-04 发布社区电池储能征询（Call for Evidence），截止 2026-07-30。参考模板为澳洲政府资助的 300+ 社区电池计划（单体容量 50 kW–5 MW）。

**核心议题：**
- 如何规模化推广社区共享电池（Community Battery）
- 如何拆除监管和商业壁垒
- 如何确保收益惠及租户、公寓住户、低收入家庭等无法自装家庭电池的群体

此举是 Warm Homes Plan 和家庭储能补贴框架之外的**新增政策工具信号**，重点解决当前政策覆盖盲区。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-06-04 | DESNZ 发布社区电池 Call for Evidence |
| **2026-07-30** | **征询截止** |
| 待定 | 政策方案公布 |

> **来源：**
> - [UK government mulls Australia-style community battery subsidy program — ESS News](https://www.ess-news.com/2026/06/04/uk-government-mulls-australia-style-community-battery-subsidy-program/) `[2026-06]`
> - [Assessing the case for community batteries: call for evidence — GOV.UK](https://www.gov.uk/government/calls-for-evidence/assessing-the-case-for-community-batteries) `[2026-06]`

### 7.8 阳台光伏合法化框架（Plug-in Solar）`[阳储]` `[政策征询中]`

#### DESNZ 首次为插电式光伏建立合规路径，明确不含储能

**政策正文概述：** DESNZ 于 **2026-06-16** 发布"插电式光伏"（Plug-in Solar）征询，首次为英国建立阳台光伏合规框架：拟修订《插头与插座（安全）条例 1994》（Plugs and Sockets etc. (Safety) Regulations 1994, PSSR），并发布《过渡期产品规范 v1.0》（Interim Product Specification）。核心技术要求：单相、最高 253V AC/50Hz；逆变器最大视在功率 **≤800VA**、最大电流 **≤3.5A**；光伏组件总直流功率上限 **2000W**，超过 960W 建议由专业人员评估线路负荷；**每户限装 1 台设备**；须通过 BS 1363 插头（5A 保险丝、局部绝缘插脚）连接。**过渡期产品规范明确不含电池储能**——这与德国（阳台光伏配储已纳入简化注册）、法国、意大利等允许阳储配套补贴的路径形成鲜明对比，意味着若征询结果延续这一限制，英国阳台光伏在合法化初期将是纯光伏产品，储能仍需另行走既有的家储合规与安装路径。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| **2026-06-16** | **DESNZ 发布 Plug-in Solar 征询（PSSR 修订 + 过渡期产品规范 v1.0）** |
| **2026-06-30** | **征询截止** |
| **2026-07-22（预计）** | **征询回应摘要发布** |

> **来源：**
> - [Plug-in solar: consultation document — GOV.UK](https://www.gov.uk/government/consultations/plug-in-solar/plug-in-solar-consultation-document-accessible-webpage) `[2026-06]`
> - [Plug-in Solar Device Interim Product Specification Version 1.0 — GOV.UK](https://assets.publishing.service.gov.uk/media/6a31167d15f2a70fac7e6026/plug-in-solar-interim-product-specification.pdf) `[2026-06]`
> - [DESNZ Opens Plug-In Solar Consultation: PSSR Amendment and Interim Product Spec — Plug Solar Hub](https://plugsolarhub.co.uk/desnz-plug-in-solar-consultation-2026) `[2026-06]`

### 7.9 动态频率响应市场规则修订 `[工商储]` `[部分已生效]`

#### Ofgem 裁定 Dynamic Response 服务条款修订，六项获批、两项被拒

**政策正文概述：** Ofgem 就 NESO（国家能源系统运营商）提交的 Dynamic Response 频率响应服务条款修订方案作出裁定：8 项提案中 6 项获批（分两批生效），2 项因"未充分征询"被拒（NESO 可补充征询后重新提交）。核心变更影响电池资产在英国频率响应市场（含 Dynamic Containment、Moderation、Regulation 等品类）的可用性认定、收益叠加规则和处罚机制，对独立参与该市场（尤其平衡机制外的中小型及聚合型电池资产）的收益构成实质约束。

**已获批变更（2026-07-31 生效）：**
- 未在平衡机制中提交有效最终物理通知（Final Physical Notification）的资产，无论实际技术能力如何，一律被认定为"Dynamic Response 不可用"
- 资产若同时签约 Stability Network Procurement Services，须采用预先核准的基线方法学，防止收益重复计费
- 可用性费用计算条款的名称调整（行政性变更）

**已获批变更（2027-01-01 生效）：**
- 未经 NESO 指令自行标记"解除武装"（disarmed）状态的服务商将被处罚
- NESO 获授权公开各服务商的处罚数据
- 非 BMU（非平衡机制单元）服务商须在合约期外同步提交运行计量和基线数据，滚动 28 天周期内达标率须 ≥80% 方可维持参与每日拍卖资格

**被拒变更：** 四档分级处罚机制、NESO 扩大暂停参与权限——均因征询程序不充分被驳回，Ofgem 表示若补充征询后可重新考虑。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-07-06 | Ofgem 发布裁定结果 |
| **2026-07-31** | **首批变更生效（可用性认定、收益叠加规则）** |
| **2027-01-01** | **第二批变更生效（解除武装处罚、非 BMU 数据提交要求）** |

> **来源：**
> - [Ofgem approves rule changes for UK frequency response markets — ESS News](https://www.ess-news.com/2026/07/06/ofgem-approves-rule-changes-for-uk-frequency-response-markets/) `[2026-07]`
> - [Ofgem approves rule changes for UK frequency response markets — PV Magazine](https://www.pv-magazine.com/2026/07/07/ofgem-approves-rule-changes-for-uk-frequency-response-markets/) `[2026-07]`

#### PM 解读

> **[2026-07-11]**
> - **SEG 分时售电 + VPP 参与 = 英国家储 App 的核心能力矩阵**：最高 50p/kWh 的 SEG 分时电价意味着储能不再只是"省电"工具，而是"赚电费"工具。App 需要三层能力：① 分时电价数据集成（Octopus、British Gas 等零售商电价 API）；② 智能充放电调度（低价充、高价放）；③ VPP 接入（参与频率响应、容量市场等辅助服务）。这三层是递进关系，至少前两层是市场准入的基本要求
> - **Warm Homes Plan 面向低收入群体，安装商 B 端工具需要适配补贴申请流程**：£150 亿预算中有大量资金通过安装商渠道落地。B 端工具（Installer App/Portal）如果能嵌入"Warm Homes Plan 资格查询 + 申请流程引导"，将是安装商选择合作品牌的加分项
> - **ECO4 于 2026-12-31 终止，ECO5 已确认取消**：政府决定终结整个 ECO 框架，£1.5B 资金重新分配至 Warm Homes Plan。渠道链路从"能源供应商分包"变为"地方政府 → 安装商"，安装商需持有 TrustMark + PAS 2030:2023 认证
> - **T-1 + T-4 合计超 1.8 GW，VPP 收益可视化应从差异化功能升级为 App 核心模块**：T-1 拍卖（576 MW，2026/27 交付）+ T-4 拍卖（1.22 GW，2029/30 交付）合计超 1.8 GW 容量市场合同，确认英国是欧洲 BESS 参与电力市场最成熟的国家。对家储 App 的含义：VPP 收益不再是"未来可能有"的叙事，而是已经发生的真实收入来源——App 首屏应该展示"昨天 VPP 帮你赚了 £X"，而不是把 VPP 功能埋在设置里等用户发现
> - **BS 7671 Amendment 4 禁止阁楼安装，重塑英国家储安装规范，安装商工具需同步升级**：历史上相当比例的英国住宅电池安装在阁楼（空间充裕、不占生活区），Amendment 4 从 2026-10-15 起强制禁止此做法，违规安装影响保险和 EPC 认证。对产品端的含义：① 硬件需充分测试车库、外墙壁挂、地下室等替代安装场景的热管理性能；② 安装商工具（Installer App）需内置"Amendment 4 合规位置核查清单"，安装前自动判断候选位置是否满足通风/逃生/维护要求，避免安装商因不了解新规而将设备装在不合规位置引发的合规与保险纠纷；③ C 端 App 的安装引导流程须更新，明确告知用户禁止安装位置并给出合规替代位置示意图
> - **社区电池征询（2026-06-04，截止 7-30）是英国政策向"无法自装用户"扩展的前置信号——C&I 产品线需在路线图上预留 50 kW–5 MW 社区电池形态**：DESNZ 征询议题框架直指现有家庭电池政策的覆盖盲区：租户、公寓住户、低收入群体。若政府跟进澳洲模式推出社区电池补贴，主力部署单元将是 50 kW–5 MW 的社区级储能系统，而非消费级家储产品。对于拥有 C&I 储能产品线的厂商，这是英国 2027-2028 年新增量的早期信号窗口：① 现阶段可向 DESNZ 提交书面证据意见（截止 7-30），展示技术能力并在政策制定层建立认知；② 软件侧提前规划"多建筑共享储能管理"的 B 端系统架构，避免后期重构成本
> - **英国首次为阳台光伏立法，但过渡规范明确排除储能——这是产品定义上的关键约束，而非可以软件绕开的限制**：DESNZ 的 Plug-in Solar 征询标志着英国从"无阳台储能政策框架"（原 7.4 所述）转向"有纯光伏合规框架，但储能仍被排除"的过渡状态。对产品策略的含义：① 若要进入英国阳台光伏市场，短期内必须先以"纯光伏、不含电池"的产品形态合规上市，储能功能需等待后续规范迭代或另行走英国现有的家储合规（G98/G99 并网许可、BS 7671 布线规范）与安装商渠道；② 800VA/3.5A 的逆变器规格与德国 800W 馈电上限高度接近，意味着微逆固件的功率钳位逻辑可直接复用，但需要针对英国 BS 1363 插头规格单独做硬件适配；③ 每户限装 1 台设备的规定应体现在英国市场的产品注册与激活流程中，避免用户叠加安装导致合规风险；④ 建议在 2026-07-22 征询回应摘要发布后，第一时间评估储能纳入的可能性和时间表，这将决定英国阳台储能是"现在布局"还是"等下一版规范"的市场进入节奏
> - **Ofgem 于 2026-06-26 发布 LDES Window 1 拟授权名单（16 项目 / 7.6 GW / 136.9 GWh），英国长时储能从"政策设计"正式进入"项目落地"阶段**：从 73 个合格项目中遴选 16 个，时长 8–22 小时，锂离子 BESS 和抽水蓄能为主，含 CAES 和全钒液流等新兴路线，征询截止 2026-08-07，正式合同预计 2026 年夏授予。对 C&I 储能产品的含义：① 英国长时储能的收益路径从"容量市场 + 频率响应（均为 2 小时内短时场景）"正式扩展为"Cap & Floor 保底机制（8-22 小时长时场景）"——B 端报价和 EMS 平台需为这两条路径提供独立的 IRR 测算模型（短时 BESS 套利 vs 长时 LDES 稳定回报）；② 7.6 GW Window 1 规模表明英国 LDES 市场体量不是试点而是系统性部署，有 B 端工商储业务的厂商应评估是否将 6-22 小时产品形态纳入英国产品矩阵；③ 正式合同授予后（2026 年夏），Cap/Floor 初始收益上下限将公开，届时可基于实际数字校正 LDES 项目的 IRR 预测区间，是 B 端 EMS 平台更新长时储能定价模型的关键时间点
> - **Ofgem 收紧 Dynamic Response 可用性认定和处罚机制，B 端聚合 EMS 需要在 7-31 前完成合规适配**：未提交有效最终物理通知即被判定"不可用"（无论实际技术能力）、非 BMU 资产须达 80% 数据提交合规率方可维持每日拍卖参与资格——这两项 7-31 生效的变更直接提高了独立/聚合电池资产参与频率响应市场的操作门槛。对有 B 端聚合业务或对接英国 VPP 聚合商 API 的厂商：① EMS 调度逻辑需要将"平衡机制物理通知提交状态"作为频率响应可用性判断的前置条件之一，避免因未同步提交通知导致收益认定为零；② 非 BMU 参与路径的运行计量/基线数据提交需要自动化、常态化（而非仅合约期内提交），滚动 28 天 80% 达标率应作为内部监控指标；③ 2027-01 生效的"解除武装"处罚及 NESO 处罚数据公开机制，意味着违规记录未来对聚合商信誉可见，服务商筛选和商务谈判时应纳入考量

---

## 八、奥地利

### 8.1 储能补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **气候与能源基金** | 光伏+储能补贴，储能部分 €150/kWh | 2025 年多轮 |
| **2025 首轮** | €1,200 万预算（实际因超额申请扩大至 €4,880 万），目标 220 MW 光伏 + 200 MWh 储能 | 2025 |
| **2025 末轮** | €800 万追加预算 | 2025-10 |
| **2026 首轮** | 原预算 €4,000 万，因超额申请扩大至 **€7,000 万**；约 29,000 份申请中 **约 90% 包含储能配置** | 2026 |
| **2026 二轮** | €1,200 万预算，按容量分四档：≤10 kW 及 10–20 kW 各 €200 万，20–100 kW 及 >100 kW 各 €400 万；≤10 kW 固定费率 €150/kW，10–20 kW 为 €140/kW，20 kW 以上按最低补贴需求竞标排序 | 2026-06-17 开放 |
| **2026 三轮** | €800 万预算 | 2026-10-08 至 10-22 |
| **欧洲制造加成** | 使用欧洲制造的组件/逆变器/储能，额外 10% "Made in Europe" 补贴；截至 2026 年，约 46% 光伏申请已采用欧洲制造逆变器 | 2025 起持续 |

- **申请条件**：储能须与新建或扩建的光伏系统一同申请，不得单独为已运行系统配储

### 8.2 阳台储能政策 `[阳储]`

- `[持续有效]` 800W 以下系统可使用 Schuko 插头安装，无需电工
- `[持续有效]` 需在 E-Control 平台注册并通知电网运营商
- `[2024]` 推出 €500 阳台光伏补贴（迅速用尽）
- 需跟踪后续年度补贴是否续期

> **来源：**
> - [Austria Allocates €12M for Solar-Plus-Storage — PV Magazine](https://www.pv-magazine.com/2025/08/20/austria-allocates-e12-million-for-solar-plus-storage-rebates/) `[2025-08]`
> - [Austria Opens Final €8M Solar-Plus-Storage Round — PV Magazine](https://www.pv-magazine.com/2025/10/08/austria-opens-final-e8-million-solar-plus-storage-rebate-round/) `[2025-10]`
> - [Austria Earmarks €35M for Battery Rebates — PV Magazine](https://www.pv-magazine.com/2024/04/11/austria-earmarks-e35-million-for-battery-rebates/) `[2024-04]`
> - [Austria allocates €12 million for solar-plus-storage rebates (2026 second round) — PV Magazine](https://www.pv-magazine.com/2026/06/15/austria-allocates-e12-million-for-solar-plus-storage-rebates-2/) `[2026-06]`
> - [Austria introduces 'Made in Europe' bonus for solar and storage projects using European components — PV Tech](https://www.pv-tech.org/austria-introduces-made-in-europe-bonus-solar-storage-european-components/) `[2026]`

#### PM 解读

> **[2026-07-11]**
> - **"Made in Europe" 10% 加成是有欧洲制造布局厂商的政策红利**：如果产品（或关键部件）在欧洲制造，App 中可以醒目展示"Made in Europe"标签和额外补贴金额，直接影响用户购买决策。对于中国厂商，这是一个值得评估的战略信号——是否需要在欧洲布局组装产能
> - **"储能必须与新建光伏捆绑申请"限制了 retrofit 市场**：已有光伏系统的用户无法单独申请储能补贴，这意味着 App 中的"光伏+储能套装推荐"比"单独配储"优先级更高。产品包装策略上，"光储一体机"在奥地利比"独立储能箱"更有政策适配性
> - **€500 阳台光伏补贴"秒光"说明需求旺盛**：2024 年 €500 补贴迅速用尽，说明奥地利阳储用户的价格敏感度高但购买意愿强。App 中可以内置"补贴开放提醒"功能，帮助用户抢窗口
> - **2026 首轮 90% 申请含储能，奥地利已从"光伏配储"市场进化为"储能主导"市场**：29,000 份申请中九成含电池，且预算从 €4,000 万一路扩容至 €7,000 万，说明当地用户已默认"装光伏=装储能"。App 端不应再向奥地利用户展示"是否要加装储能"的选择分支，应默认捆绑呈现光储一体报价和 ROI，把决策成本从"要不要储能"转移到"选多大容量"
> - **三档补贴窗口（6-17、10-8~10-22）叠加超额扩容的历史规律，App 应内置"申请窗口倒计时+预算消耗预警"**：过去三轮均出现预算超额扩容（€1,200 万→€4,880 万、€4,000 万→€7,000 万），意味着奥地利用户抢补贴窗口的行为模式稳定。安装商工具和 C 端 App 应在每轮窗口开放前主动推送提醒，并展示"历史扩容概率"来强化用户尽快申请的动机

---

## 九、瑞士

### 9.1 光伏+储能政策 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **Pronovo 平台** | 管理可再生能源补贴分配和拍卖 | 持续有效 |
| **自消费激励** | 新法规鼓励通过储能电池或电动汽车扩大自消费比例，削减注入电网高峰 | 2026 生效 |
| **本地电力共同体（LEG）** `[新增]` | 同一电网区域、同一电压等级、同一市镇内的消费者可组建"本地电力共同体"（Lokale Elektrizitätsgemeinschaft），共享自产电力并享受电网使用费折扣（低压网络折扣 40%，占用变压器网络折扣 20%）；配电网运营商（VNB）须为所有终端用户、储能运营商、发电者按计量点开具计量费账单 | **2026-01-01 起施行** |
| **储能电网费退款激励** `[新增]` | 具备终端用电能力的储能运营商可自 2026-01-01 起向 VNB 申请电网使用费退款，退款按小时现货市场电价计算，形成"低电价时段充电、避免高价时段馈网"的经济激励 | **2026-01-01 起施行** |
| **冬季发电奖金** | 对冬季发电的光伏系统给予额外补贴 | 2025-11 |
| **市场规模** | BTM 电池累计 2,461 MWh，过去一年新增 1,010 MWh（同比 +82%） | 2025 |

- 非 EU 成员国，独立制定能源政策
- 各州（Canton）可能有额外的地方补贴
- `[2026-01-01 起]` 新法规允许本地电力交易（local electricity trading），LEG 框架是其具体落地形式

### 9.2 阳台/便携储能 `[阳储]` `[移储]`

- 无专项法规，遵循瑞士电气安全标准
- 各州政策差异大，需逐一跟踪

> **来源：**
> - [Switzerland Expands Rules for Rooftop Solar, Storage, Energy Communities — PV Magazine](https://www.pv-magazine.com/2025/02/24/switzerland-expands-rules-for-rooftop-solar-storage-energy-communities/) `[2025-02]`
> - [Switzerland Introduces Winter Electricity Bonus — PV Magazine](https://www.pv-magazine.com/2025/11/27/switzerland-introduces-winter-electricity-bonus-for-solar-installations/) `[2025-11]`
> - [Switzerland Deploys 1.52 GW of Solar in 2025 — PV Magazine](https://www.pv-magazine.com/2026/04/08/switzerland-deploys-1-52-gw-of-solar-in-2025/) `[2026-04]`
> - [Strommarkt 2026: Was sich in der Schweiz ändert — energy unlimited](https://www.energyunlimited.ch/solar-ratgeber/strommarkt-2026-was-sich-in-der-schweiz-aendert) `[2026]`
> - [Neun Fakten zu den Rückliefertarifen 2026 — EKZ](https://www.ekz.ch/de/blue/wissen/2025/rueckliefertarife-2026.html) `[2025]`

#### PM 解读

> **[2026-07-04]**
> - **本地电力交易（P2P Energy Trading）是前沿软件场景**：2026 新法规允许本地电力交易，这意味着家储用户未来可以"把多余的电卖给邻居"。App 需要预留 P2P 交易接口——虽然短期不会大规模落地，但这是继 VPP 之后家储软件的下一个大方向。Sonnen 的 sonnenCommunity 在德国已经做了类似探索
> - **冬季发电奖金推动"季节性智能调度"**：冬季发电额外补贴意味着 App 的充放电策略需要有季节感知——冬季优先馈电（享受奖金），夏季优先自消费。这对 AI 调度算法提出了更细粒度的要求
> - **BTM 电池 +82% 同比增长说明市场正在起飞**：瑞士虽然不是 EU 成员国，但高购买力+高电价+政策友好使其成为值得关注的高端市场。注意瑞士不适用 EU 电池法规，产品合规需要走独立路径
> - **LEG 框架 + 现货价电网费退款正式落地（2026-01-01），BMS/EMS 需要"社区身份识别 + 现货价套利"双引擎**：LEG 明确了"本地电力共同体"的组建条件（同电网区域/同电压等级/同市镇）和折扣力度（低压 40%、变压器网络 20%），储能运营商额外可按小时现货价申请电网费退款。这意味着瑞士家储 EMS 需要同时具备两层逻辑：① 判断用户是否属于某个 LEG 及其对应折扣档位（低压/变压器网络），动态调整"本地共享优先"vs"自用优先"的调度策略；② 独立于 LEG 之外，仍可基于小时现货价做纯粹的充放电套利并申请电网费退款。建议 EMS 算法把"LEG 归属识别"作为瑞士市场的必选前置模块，而非选装功能——折扣差异（40% vs 20%）直接影响调度策略的经济最优解

---

## 十、比利时

### 10.1 法兰德斯（Vlaanderen）`[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **Prosumertarief** | 产消者关税：安装储能可显著降低峰值注入，从而减少该税费 | 持续有效 |
| **电池补贴终止** | 法兰德斯电池补贴（Battery Premium）已于 2025-01-01 终止 | 2025-01 终止 |
| **净计量** | `[2024]` 取消净计量，推动储能需求增长 | 2024 |

- 法兰德斯是欧洲最强的住宅光伏+储能市场之一（储能同时降低 Prosumertarief 并提升自消费率）

### 10.2 瓦隆（Wallonie）`[家储]`

- 正在推动简化审批和激励性投资框架
- 当前无专门的住宅储能补贴计划，聚焦大型 BESS 项目

### 10.3 布鲁塞尔首都区 `[家储]`

- 独立的能源政策，需单独跟踪补贴方案

### 10.4 阳台储能 `[阳储]`

- 各大区政策不同，需分别确认合规要求
- 法兰德斯净计量取消后，阳台储能配储需求上升

> **来源：**
> - [Belgium Solar Incentives 2025: Regional Guide — SurgePV](https://www.surgepv.com/hub/solar-industry/belgium) `[2025]`
> - [Belgium's Flanders Region Solar Rebates — PV Magazine](https://www.pv-magazine.com/2023/04/20/belgiums-flanders-region-launches-new-call-for-solar-rebates/) `[2023-04]`

#### PM 解读

> **[2026-06-14]**
> - **法兰德斯的 Prosumertarief 是"储能即省税"的典型政策场景**：用户安装储能后，峰值注入降低 → Prosumertarief 税费减少。App 中需要可视化"安装储能前后的 Prosumertarief 对比"和"年化节省金额"，这是最有说服力的购买理由。不是"你省了多少电费"，而是"你少交了多少税"
> - **三区政策割裂增加了软件本地化成本**：法兰德斯、瓦隆、布鲁塞尔三区政策独立，意味着 App 中的补贴信息、电价数据、合规要求需要按区域适配。如果资源有限，建议优先法兰德斯（市场最大、储能经济性最强）
> - **法兰德斯电池补贴已终止，但储能需求反而因净计量取消而上升**：2024 取消净计量 → 2025 取消电池补贴，看似利空，但净计量取消后自消费率成为核心回报驱动力，储能需求反而更刚性。这是"补贴退坡但市场自驱"的典型案例

---

## 十一、波兰

### 11.1 住宅储能补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **Mój Prąd 6.0** | 第六期"我的电力"计划，总预算 PLN 18.5 亿（约 €4.3 亿），原预算 PLN 4 亿因超额需求扩大 4.5 倍 | 2024-09 启动 |
| **储能补贴额度** | 额外 PLN 16,000（约 €3,750）用于配套储能系统 | 2024-2025 |
| **申请情况** | 共 12.1 万份申请，其中 7.4 万份（60%）包含储能 | 2025 统计 |
| **平均储能容量** | 约 5 kWh | 2025 |
| **Mój Prąd 7.0** | 已于 2026-03-30 启动，预算 PLN 3 亿（约 €7,000 万），聚焦储能，详见下方 | 2026-03-30 已启动 |

### 11.2 大型储能 `[通用]`

- `[2025-04]` PLN 41.5 亿（约 €9.6 亿）大型储能补贴计划开放申请
- `[2025-12]` 172 个项目共 14.5 GWh 获得补贴，要求 2028 年底前建设完成

### 11.3 阳台储能 `[阳储]`

- Mój Prąd 计划适用于小型光伏+储能组合，阳台储能配储可申请

> **来源：**
> - [Poland Allocates Record Budget for Home Solar, Storage — PV Magazine](https://www.pv-magazine.com/2025/09/15/poland-allocates-record-budget-for-home-solar-storage-rebate-scheme/) `[2025-09]`
> - [Poland's $1B Energy Storage Subsidy Opens — PV Magazine](https://www.pv-magazine.com/2025/04/04/polands-1-billion-energy-storage-subsidy-scheme-opens-for-applications/) `[2025-04]`
> - [Poland Allocates Subsidies to 14.5 GWh — PV Magazine](https://www.pv-magazine.com/2025/12/19/poland-allocates-subsidies-to-14-5-gwh-of-energy-storage-projects/) `[2025-12]`
> - [Poland Solar Subsidies 2025 — SurgePV](https://www.surgepv.com/hub/solar-industry/poland) `[2025]`

#### Mój Prąd 7.0 详情 `[已启动]`

**政策正文概述：** 官方名称调整为"家庭储能资助计划"（Finansowanie domowych magazynów energii），与前六期最大差异在于**完全以储能系统为主体**——不单独资助新建光伏，现有光伏用户方可搭配申请储能补贴。计划分两部分实施：**Part 1**（由 KPO/欧盟复苏基金资助，2026-03-30 启动）已于 **2026-06-19** 结束申请受理；**Part 2**（PME 部分二，由"现代化基金"资助）已明确具体方案，预计 2026 年秋季（9 月前后）开放申请。Part 1 补贴额度按用户结算方式分档：net-billing（净结算）用户最高 **PLN 16,000**，net-metering（净计量，旧制）用户最高 **PLN 8,000**，预算约 PLN 3 亿（约 €7,000 万），主要覆盖已完成安装但错过前期申请窗口的项目。Part 2 总预算扩大至 **PLN 20 亿**，补贴比例最高覆盖成本的 **30%**（不超过 **PLN 800/kWh**），要求储能标称容量 **≥10 kWh** 且须配备能源管理系统（EMS）和离网运行能力，费用可追溯期为 **2025-11-01** 之后完成的项目。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2026-02-05 | 公众咨询结束 |
| **2026-03-30** | **Part 1（KPO 资金）正式启动，开放申请** |
| **2026-06-19** | **Part 1 申请窗口关闭** |
| **2025-11-01** | **Part 2 费用可追溯起始日（覆盖已完成但未及申请的项目）** |
| **2026 年内（预计 9 月）** | **Part 2（"现代化基金"资助，预算 PLN 20 亿）预计开放申请：补贴≤30%成本/≤PLN 800/kWh，要求≥10 kWh 容量 + EMS + 离网能力** |

> **来源：**
> - [Program Mój Prąd 7.0 powraca! — SWATT](https://swatt.pl/pl/SWATT_WIEDZY/dofinansowania/program-moj-prad-70-powraca-w-2026-rzad-finansuje-magazyny-energii-i-ciepla) `[2026]`
> - [Czy będzie Mój Prąd 7.0? — Sunergo](https://sunergo.pl/blog/czy-bedzie-moj-prad-7-0-co-juz-wiemy-o-programie-i-kiedy-moj-prad-2026-startuje/) `[2026]`
> - [Mój Prąd 7.0 – zasady i dotacje na magazyny energii 2026 — SunSol](https://sunsol.pl/dofinansowanie-fotowoltaiki/moj-prad-7-0-zasady-programu/) `[2026]`
> - [Nowy start programu Mój Prąd 7.0 — Alians OZE](https://alians-oze.pl/moj-prad-7-dotacje-magazyny-energii-2026/) `[2026]`
> - [Nowy start programu Mój Prąd 7.0 – co zmieni się dla prosumentów w 2026 r.? — Alians OZE](https://alians-oze.pl/moj-prad-7-dotacje-magazyny-energii-2026/) `[2026-06]`
> - [Przydomowe magazyny energii — Fundusz Modernizacyjny — Portal Gov.pl](https://www.gov.pl/web/funduszmodernizacyjny/przydomowe-magazyny-energii) `[2026-07]`
> - [Druga szansa na dotację do magazynu energii i PV. NFOŚiGW wznawia nabór po programie Mój Prąd — GLOBENERGIA](https://globenergia.pl/druga-szansa-na-dotacje-do-magazynu-energii-i-pv-nfosigw-wznawia-nabor-po-programie-moj-prad/) `[2026-07]`

#### PM 解读

> **[2026-07-05]**
> - **Mój Prąd 60% 含储能，波兰是欧洲储能渗透率增长最快的市场之一**：12.1 万份申请中 7.4 万含储能，说明波兰用户对"光伏+储能"套装的接受度已经非常高。App 的波兰语本地化应该进入优先级序列
> - **平均 5 kWh 容量段说明市场偏好小型系统**：波兰用户倾向于小容量储能（对标德国的 Balkonkraftwerk 配储场景），产品定义上 5-10 kWh 的入门级家储是主力 SKU。App 中的容量推荐算法需要适配波兰的用电模式和电价水平
> - **Mój Prąd 7.0 已于 2026-03-30 启动，但预算缩水 16 倍，补贴申请功能需重新定位**：7.0 实际预算约 PLN 3 亿（6.0 为 PLN 18.5 亿），且面向的是"已装光伏、尚未申请储能补贴"的存量补录用户，而非新装用户。App 内置的"补贴申请引导"功能仍有价值，但目标用户画像必须调整——不是帮新买家申请补贴，而是帮"有光伏没储能"的老用户找到过渡计划的入口。由于预算有限，额度可能快速耗尽，App 需内置"补贴剩余额度提醒"功能
> - **PLN 41.5 亿大型储能补贴说明波兰正在构建储能产业生态**：大型储能项目的落地将带动配套的 EMS、SCADA 等 B 端软件需求。对于有 B 端储能管理平台的厂商，波兰是值得关注的增量市场
> - **Mój Prąd 7.0 Part 1 已于 6-19 关闭，补贴按结算方式分档（net-billing PLN 16,000 vs net-metering PLN 8,000）——App 补贴计算器需要按用户结算类型分支**：Part 1 关闭意味着当前窗口的补录用户申请已结束，产品运营需立即将资源转向 Part 2（现代化基金资助）的时间线跟踪。同时首次明确的分档金额差异（净结算用户补贴是净计量用户的 2 倍）说明波兰政府在通过补贴力度引导用户从旧的净计量向净结算迁移。App 内的"补贴查询/计算器"功能必须先判断用户当前的电费结算方式，再展示对应的补贴上限，避免因笼统展示单一金额造成用户预期错位
> - **PME Part 2 明确 PLN 20 亿预算和"≥10 kWh + EMS + 离网能力"技术门槛，预算规模较 Part 1 扩大近 7 倍——波兰家储正从"补贴驱动的小额补录"升级为"技术合规驱动的规模化支持"**：与 Part 1（PLN 3 亿，无硬性技术门槛）相比，Part 2 首次将 EMS 配置和离网运行能力作为申领资格的强制要求，且费用可追溯至 2025-11-01。对产品端的行动：① 入门级 SKU（5 kWh 左右，见此前 PM 解读关于"5 kWh 甜点段"的判断）若不满足 ≥10 kWh 门槛，需在波兰市场推出满足新门槛的进阶 SKU，否则用户无法申领 Part 2 补贴；② App/固件的 EMS 模块和离网运行能力需要作为波兰市场的强制配置项，而非可选功能，直接关系产品能否进入补贴目录；③ 申请窗口预计 9 月开启，建议 Q3 前完成产品认证材料准备，避免错过窗口开放初期的申请高峰

---

## 十二、捷克

### 12.1 储能补贴 `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **2026 新政** | 覆盖并网接入、补贴支持、市场准入三个维度的完整框架 | 2026-01 生效 |
| **补贴比例** | 最高可达项目总投资的 50% | — |
| **补贴上限** | 每个项目最高 €300 万 | — |

### 12.2 阳台/便携储能 `[阳储]` `[移储]`

- 需跟踪新框架下对小型即插即用系统的具体规定

> **来源：**
> - [Battery Energy Storage Systems Czech Republic Regulation 2026 — CopowBattery](https://www.copowbattery.com/news/battery-energy-storage-systems-regulations-85281334.html) `[2026]`

#### PM 解读

> **[2026-06-14]**
> - **50% 补贴 + €300 万上限主要利好商用/工业储能**：住宅级储能很难触及 €300 万上限，这个框架对 C&I（商工业）储能更有吸引力。对于有 B 端储能管理平台的厂商，捷克是 2026 年值得优先评估的中东欧市场
> - **新框架刚生效（2026-01），政策执行细则仍需跟踪**：框架落地后的具体操作层面（申请流程、审批时间、技术要求）还在成型中，不建议立即重仓投入，但可以先接触当地安装商渠道建立关系

---

## 十三、北欧四国

### 13.1 总体特征

- 四国均**适用标准增值税**（无太阳能/储能 VAT 减免）
- 市场驱动为主，依靠电力市场价差和电网服务收入支撑储能投资回报
- 无大规模住宅储能专项补贴

### 13.2 瑞典 `[家储]`

- 北欧住宅储能最发达市场，拥有最大的 BTM 电池装机和 BESS 项目管线
- `[2025]` 大量 BESS 项目推进中，市场投资回报"极具吸引力"

### 13.3 芬兰 `[家储]`

- `[2025]` BESS 部署大幅增长，与瑞典共同领跑北欧
- 智能供暖+热泵+储能的灵活性管理发展领先

### 13.4 挪威 `[家储]`

- BESS 部署滞后于瑞典和芬兰
- 电价结构和水电资源丰富削弱了住宅储能经济性

### 13.5 丹麦 `[家储]`

- EV+光伏的灵活性管理发展领先
- 需跟踪住宅储能的独立政策进展

### 13.6 阳台/便携储能 `[阳储]` `[移储]`

- 北欧四国无针对阳台储能的专项法规，市场规模有限
- 需遵循各国电气安装标准

> **来源：**
> - [Sweden and Finland Surge Ahead for BESS — Energy Storage News](https://www.energy-storage.news/sweden-and-finland-surge-ahead-of-norway-for-bess-deployments/) `[2025]`
> - ['Extremely Attractive Revenues' for BESS in Nordics — Energy Storage News](https://www.energy-storage.news/extremely-attractive-revenues-for-bess-in-nordics-as-sens-and-ilmatar-progress-sweden-projects/) `[2025]`
> - [Solar VAT Rates in Europe 2026 — SurgePV](https://www.surgepv.com/blog/solar-vat-rates-europe) `[2026]`

#### PM 解读

> **[2026-06-14]**
> - **北欧是"市场驱动型"市场，App 的电力市场套利能力是核心竞争力**：没有补贴兜底，用户完全靠电力市场价差赚回投资。App 必须支持实时电价数据（Nord Pool）和自动化的"低价充+高价放"策略。能做好这一层的产品，在北欧的用户留存和口碑会远好于只做基础监控的竞品
> - **瑞典是北欧首选市场**：最大的 BTM 装机量 + 最大的项目管线 + "极具吸引力"的投资回报，瑞典应该是北欧市场拓展的第一站。App 瑞典语本地化优先于芬兰语/挪威语/丹麦语
> - **芬兰的"热泵+储能"灵活性管理是产品差异化方向**：芬兰在智能供暖+储能的联动管理上领先，这对 App 的智能家居集成能力提出要求——不只是管电池，还要管热泵。如果产品能支持"热泵+储能"联合调度，在芬兰市场会有显著差异化优势
> - **挪威暂不优先**：水电资源丰富+低电价结构使住宅储能经济性较弱，短期 ROI 不明朗

---

## 十四、其他欧洲国家

| 国家 | 适用品类 | 状态概述 | 信息时间 |
|------|---------|---------|---------|
| **爱尔兰** | `[家储]` | 已建立完整的储能监管框架 | 截至 2025-04 |
| **葡萄牙** | `[家储]` | 已建立完整的储能监管框架 | 截至 2025-04 |
| **希腊** | `[家储]` | 储能政策早期阶段 | 截至 2025-04 |
| **罗马尼亚** | `[工商储]` | EC 批准 €1.5 亿独立储能补贴计划（现代化基金） | 2026-03 |
| **匈牙利** | `[家储]` `[工商储]` | 已推出 HUF 1,000 亿住宅储能补贴计划（详见 14.2） | 2025-12 |

> **来源：**
> - [EU Members Make Mixed Progress on Energy Storage — Energy Storage News](https://www.energy-storage.news/european-union-members-make-mixed-progress-in-implementing-energy-storage-strategies/) `[2025-04]`

### 14.1 罗马尼亚独立储能补贴 `[工商储]`

#### EU 现代化基金补贴计划 `[已批准]`

**政策正文概述：** 欧盟委员会于 2026-03-09 批准罗马尼亚 **€1.5 亿**独立储能补贴计划（通过 EU 现代化基金资助），目标部署至少 **2,174 MWh** 独立储能。每 MWh 最高补贴 €69,000，单项目上限 €1,500 万，最高覆盖 100% 合规成本。竞争性招标，部署须于 2030 年前完成。

> **来源：**
> - [European Commission approves Romania's battery storage subsidy scheme — ESS News](https://www.ess-news.com/2026/03/09/european-commission-approves-romanias-battery-storage-subsidy-scheme/) `[2026-03]`
> - [Commission approves €150 million Romanian State aid scheme — EC](https://ec.europa.eu/commission/presscorner/detail/en/ip_26_524) `[2026-03]`

### 14.2 匈牙利住宅储能补贴 `[家储]` `[工商储]` `[已实施]`

#### HUF 1,000 亿住宅储能补贴计划

**政策正文概述：** 匈牙利政府于 **2025-12** 宣布 **HUF 1,000 亿**（约 €2.6 亿/$3.05 亿）住宅储能补贴计划，面向已装或计划安装光伏的家庭，目标是提升家庭能源自给率。补贴为一次性无偿资助，每户最高 **HUF 250 万**，可覆盖约 HUF 320 万电池+逆变器系统成本的 **80% 以上**。技术要求：储能标称容量 **≥10 kWh**、直流耦合（DC-coupled）、高压（high-voltage）系统、支持**零馈网运行**。与住宅计划同步，面向企业和工业用户的储能补贴（总额 **HUF 2,300 亿**）已开放申请，Jedlik Ányos 能源计划下另有 **HUF 500 亿**工业储能专项激励，住宅与工商业两端政策同步落地。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025-12 | 匈牙利政府宣布 HUF 1,000 亿住宅储能补贴计划 |
| **2026-01-12 至 2026-02-15** | **住宅补贴申请窗口开放** |

> **来源：**
> - [Hungary launches $305 million subsidy for residential battery storage — pv magazine International](https://www.pv-magazine.com/2025/12/12/hungary-launches-huf-100-billion-subsidy-for-residential-battery-storage/) `[2025-12]`
> - [Hungary announces residential battery energy storage subsidy program — ESS News](https://www.ess-news.com/2025/12/11/hungary-announces-residential-battery-energy-storage-subsidy-program/) `[2025-12]`
> - [New Grant for Renewable Energy Production and Storage Announced — PwC Hungary](https://www.pwc.com/hu/en/pressroom/2025/uj_megujulo_energiatermelest_es_tarolast_tamogato_palyazat.html) `[2025]`

#### PM 解读

> **[2026-07-05]**
> - **爱尔兰和葡萄牙已有完整框架，值得评估进入时机**：两国框架完善但市场规模有限，适合作为"德国+意大利"之后的第二梯队市场。可以先通过当地安装商渠道小批量试水
> - **东南欧（希腊、罗马尼亚、匈牙利）仍在早期，暂不投入**：政策不明朗+市场规模小，软件本地化的 ROI 不合算。持续跟踪即可
> - **罗马尼亚从"早期阶段"升级为"有实质补贴机制"——EU 现代化基金 €1.5 亿是中东欧储能政策落地的先行案例，B 端工商储厂商可纳入 2026-2027 评估序列**：EC 批准后，罗马尼亚最高 100% 成本覆盖 + 15M 上限的竞争性招标对大型独立 BESS 项目吸引力显著；2030 年前部署要求意味着项目窗口为 3-4 年。对有 B 端储能管理平台的厂商，罗马尼亚可作为波兰之外的第二个中东欧优先市场进行接触性评估
> - **匈牙利从"政策早期阶段"跃升为中东欧最具补贴强度的住宅储能市场之一，单户最高 HUF 250 万（覆盖系统成本 80%+）——应立即纳入中东欧市场评估序列**：与波兰 Mój Prąd（PLN 16,000/户）、罗马尼亚（工商储为主）相比，匈牙利住宅补贴的单户覆盖比例显著更高，且技术门槛（≥10 kWh、直流耦合、高压、零馈网）明确指向中大型家储系统而非入门级产品线。对产品策略：① 匈牙利语 App 本地化和当地安装商渠道接触应纳入 2026 H2 评估计划；② 首轮申请窗口仅 1 个月（2026-01-12 至 02-15），若后续开放第二轮，需提前准备"补贴申请引导"功能帮用户抢窗口；③ 住宅（HUF 1,000 亿）与工商业（HUF 2,300 亿 + Jedlik Ányos HUF 500 亿）补贴同步落地，意味着 B 端储能管理平台也应同步评估匈牙利市场机会，避免只做 C 端布局

---

## 十五、澳大利亚

### 15.1 联邦层面 — Cheaper Home Batteries Program `[家储]`

| 项目 | 内容 | 时间 |
|------|------|------|
| **启动时间** | 联邦电池补贴计划启动 | 2025-07-01 |
| **扩大资金** | 总资金扩大至最高 $72 亿澳元（至 2030 年） | 2025-12 宣布 |
| **适用容量** | 标称容量 5–100 kWh，补贴适用可用容量最高 50 kWh | — |
| **安装要求** | 必须配合新建或现有屋顶光伏系统 | — |
| **安装商资质** | 必须由 SAA（Solar Accreditation Australia）认证安装商安装 | — |
| **并网要求** | 并网系统安装时必须具备 VPP 能力 | — |

### 15.2 2026 阶梯补贴结构（2026-05-01 起）`[家储]`

| 容量段 | STC 系数 | 折算约 | 说明 |
|--------|----------|--------|------|
| 0–14 kWh | 6.8 STCs/kWh（全额） | ~$252/kWh | 主力补贴段 |
| 14–28 kWh | 4.08 STCs/kWh（60%） | ~$151/kWh | 中段递减 |
| 28–50 kWh | 1.02 STCs/kWh（15%） | ~$38/kWh | 大容量段大幅缩水 |

- `[2026-05-01]` 补贴折扣计算方式调整，补贴随时间递减速度加快
- 补贴金额每半年递减一次，至 2030 年底结束
- 遵守《最佳实践指南：电池储能设备》及各州/领地电气安全法规

### 15.3 州级政策 `[家储]`

| 州 | 政策 | 状态 |
|----|------|------|
| **新南威尔士（NSW）** | VPP 激励：**2025-07-01 起升级为一次性前置支付**，2–28 kWh 电池最高 **$1,500**（典型 10 kWh 约 $1,100），可与联邦 CHB 补贴叠加；**2026-07-01 起 PDRS BESS2 准入容量上限从 28 kWh 扩大至 50 kWh**，但激励金额仍按前 28 kWh 可用容量计算封顶（>28 kWh 部分不再额外计入），电池须在 CEC 清单在册 | 有效（电池补贴已终止，仅 VPP 激励存续；准入容量扩大） |
| **维多利亚（VIC）** | 免息贷款计划（Solar Victoria）**已关闭**；2026-07-01 起补贴收入门槛从 $210,000 降至 **$150,000** | 收紧中 |
| **昆士兰（QLD）** | Battery Booster Loan and Rebate：免息贷款最高 $6,000 + 补贴最高 $3,000 | **已关闭** |
| **南澳（SA）** | REPS 认证 VPP 补贴，最高 $2,050；⚠️ 2026-04-07 起 VPP1 暂停，2026-05-05 起非优先群体无法申请，仅 Amber SmartShift 优先群体可申 | 收紧中 |
| **西澳（WA）** | 需跟踪具体方案 | 待确认 |

> **来源（州级政策更新）：**
> - [Understanding REPS in South Australia and what's changing in 2026 — MAC Trade Services](https://mactradeservices.com.au/understanding-reps-in-south-australia-and-whats-changing-in-2026) `[2026]`
> - [Solar Battery Rebate VIC — Zero Energy Australia](https://zeroenergygroup.com.au/solar-battery-rebate-victoria-everything-you-need-to-know-before-applying-2026-edition/) `[2026]`
> - [NSW turbocharges home battery savings with new incentive scheme — Clean Energy Council](https://cleanenergycouncil.org.au/news-resources/nsw-turbocharges-home-battery-savings-with-new-incentive-scheme) `[2025-07]`
> - [NSW VPP Battery Incentive 2026 — Solar Battery Outlet](https://solarbatteryoutlet.com.au/nsw-vpp-battery-incentive-2026/) `[2026]`
> - [The new rules for NSW solar battery rebates in 2026 — Solax Power](https://au.solaxpower.com/blogs/the-new-rules-for-nsw-solar-battery-rebates-in-2026.html) `[2026-07]`
> - [New South Wales Battery Rebates (PDRS) / BESS2 VPP Rebate for Batteries — Amber Electric](https://help.amber.com.au/hc/en-us/articles/31159992778893-New-South-Wales-Battery-Rebates-PDRS-BESS2-VPP-Rebate-for-Batteries) `[2026-07]`

### 15.4 阳台/便携储能 `[阳储]` `[移储]`

- 澳洲无阳台储能（Balkonkraftwerk）概念和政策框架
- 便携储能按消费电子产品管理，无专项补贴
- 需符合 AS/NZS 标准和 RCM 认证

> **来源：**
> - [Federal Solar Battery Rebate 2026 Guide — 1Komma5](https://1komma5.com/au/batteries/solar-battery-rebate-guide/) `[2026]`
> - [Australia Battery Rebates Changed May 2026 — Solahart](https://solahart.com.au/knowledge-base/australia-battery-rebates-changed-1st-may-2026-what-you-need-know) `[2026-05]`
> - [Solar Battery Rebates by State — SolarQuotes](https://www.solarquotes.com.au/battery-storage/rebates/) `[2026]`
> - [Solar & Battery Rebates 2026 — SolarQuotes](https://www.solarquotes.com.au/rebates-subsidies/) `[2026]`
> - [Federal Battery Rebate — Solar Choice](https://www.solarchoice.net.au/learn/solar-rebates/government-battery-rebate/) `[2026]`
> - [Changes to Cheaper Home Batteries — Solar Choice](https://www.solarchoice.net.au/learn/solar-rebates/government-battery-rebate/changes-1-may-2026/) `[2026-05]`

### 15.5 VPP 政策与市场 `[家储]`

#### AEMC Dispatch Mode（VPP 竞价框架） `[制度制定中]`

**政策正文概述：** AEMC 终局裁定（2025-01）确立"调度模式"（Dispatch Mode），允许 VPP/聚合商以分布式资源池直接在 NEM 批发市场竞价，与煤电气电同台。AEMC 建模：若聚合资源全面参与，2027-2050 年可节省系统性成本约 AUD 8.34 亿。

**进展追踪：**
| 时间 | 事件 |
|------|------|
| 2025-01 | AEMC 终局裁定，确立 Dispatch Mode |
| **2026-04** | **$5,000 万早期参与激励开放**（覆盖早期接入的技术与合规成本） |
| **2027-05** | **正式调度模式生效，VPP 批发市场竞价启动** |

#### VPP 市场现状（截至 2026 Q1）

| 指标 | 数值 |
|------|------|
| NEM VPP 容量 | **900 MW**（2024 年初约 350 MW，增长 >150%） |
| 活跃 VPP 运营商 | 10+ 家 |
| 全国活跃 VPP 项目 | 12+ 个 |
| 家储用户年 VPP 收益 | **$300–$1,000+**（因计划和容量而异） |

**西澳（WA）新规：** 更新 WEM Procedure，要求逆变器默认具备并网交互能力（grid-interactive by default），不符合要求的储能系统将被排除在 VPP 激励机制之外。

> **来源：**
> - [New rules allow VPPs to compete in Australia's energy market from 2027 — PV Magazine](https://www.pv-magazine.com/2025/01/09/new-rules-allow-vpps-to-compete-in-australias-energy-market-from-2027/) `[2025-01]`
> - [AEMC energy market reform: VPP dispatch mode — PV Tech](https://www.pv-tech.org/australia-aemc-consumer-energy-rule-change/) `[2025]`
> - [VPP Offers in Australia 2026 — Energy Matters](https://www.energymatters.com.au/vpp-offer/) `[2026]`
> - [Virtual Power Plants in Australia: 2026 Guide — Australian Battery Quotes](https://australianbatteryquotes.com.au/vpp-australia-2026-guide/) `[2026]`
> - [Best VPP Plans Australia 2026 Compared — Gridly](https://www.gridly.com.au/blog/best-vpp-plans-australia) `[2026]`
> - [Is Your Battery VPP-Ready? Smart Inverters Matter in 2026 — Energy Matters](https://www.energymatters.com.au/renewable-news/battery-vpp-ready-smart-inverters-australia/) `[2026]`

### 15.6 市场动态 `[通用]`

**CHB 计划执行数据：**

| 指标 | 数值 |
|------|------|
| 峰值安装速度 | **>1,500 套/日** |
| 用户平均安装容量 | 较计划启动前**翻倍** |
| 原 $23 亿预算 | 预计 2026-06 耗尽（较原计划提前 ~3.5 年） |
| 扩资后预算 | **$72 亿**（至 2030 年） |
| 2030 年目标 | 超 200 万户安装，新增约 40 GWh |
| **累计安装量（截至 2026-06）** | **超 40 万套，约 11.2 GWh 分布式储能容量**（2025-07-01 计划启动） |

**AEMO 关键数据（2026 澳洲能源周，CEO Daniel Westerman 主旨演讲）：**

| 指标 | 数值 |
|------|------|
| 住宅电池总量 | **>60 万套** |
| 被动电池峰值减负 | 每套较纯光伏用户少取电 **~1.4 kW**（减负 ~80%） |
| 2025 Q1 以来新增大型 BESS | **4,445 MW**（NEM 总装机翻倍） |
| NEM 平均电池放电量 | **359 MW**（一年前 98 MW，增至 3 倍） |
| 放电历史记录 | 3,556 MW（2026-01-07） |

AEMO CEO 表示"对被动家庭电池对系统的正面冲击规模感到意外"，正据此修订电网容量规划基础假设。

> **来源：**
> - [Why the government is overhauling its Cheaper Home Batteries Program — Canstar](https://www.canstar.com.au/energy/why-the-government-is-overhauling-its-cheaper-home-batteries-program/) `[2026]`
> - [Six Months of the Cheaper Home Batteries Program — energy.gov.au](https://www.energy.gov.au/news/six-months-cheaper-home-batteries-program) `[2026]`
> - [Cheaper Home Batteries Program Expansion: What's New in 2026 — EcoFlow AU](https://energy.ecoflow.com/au/blog/cheaper-home-batteries-program) `[2026]`
> - [More Australians to benefit from Cheaper Home Batteries — energy.gov.au](https://minister.dcceew.gov.au/bowen/media-releases/more-australians-benefit-cheaper-home-batteries) `[2026]`
> - [AEMO CEO speech at Australian Energy Week 2026 — PV Magazine Australia](https://www.pv-magazine-australia.com/2026/06/12/aemo-ceo-speech-at-australian-energy-week-2026/) `[2026-06]`
> - [Australia's battery storage fleet triples daily load-shifting as 4.4GW comes online — Energy-Storage.News](https://www.energy-storage.news/australias-battery-storage-fleet-triples-daily-load-shifting-as-4-4gw-comes-online-in-q1-2026-says-aemo/) `[2026-04]`
> - [350,000 installations in 10 months under Cheaper Home Batteries Program — PV Magazine Australia](https://www.pv-magazine-australia.com/2026/05/01/350000-installations-in-10-months-under-cheaper-home-battery-program/) `[2026-05]`

#### PM 解读

> **[2026-07-03]**
> - **VPP 能力是澳大利亚家储的硬性市场准入门槛**：联邦补贴明确要求并网系统"必须具备 VPP 能力"。这不是"有了加分"，而是"没有就拿不到补贴"。App/固件必须内置 VPP 协议栈（支持澳洲主流 VPP 聚合商接口），否则产品在澳洲市场直接失去竞争力。Tesla、Sonnen、Enphase 在这块已经成熟，是硬门槛
> - **14 kWh 甜点成立，但平均装机容量翻倍是重要信号——容量推荐算法不能只推 14 kWh**：阶梯补贴结构（0-14 kWh 全额，14-28 kWh 六折）使 13.5-14 kWh 依然是"补贴最优"选项，但用户平均装机容量翻倍表明相当比例用户主动选择更大容量——他们在用"补贴覆盖以外的自付成本"换取更长的 VPP 收益期。App 的容量推荐页需要同时呈现两个场景："补贴最大化方案（14 kWh）"和"VPP 收益最大化方案（XX kWh）"，用数字让用户自主决策
> - **州级政策正在收缩（VIC/QLD 已关闭），联邦补贴成为唯一支撑**：多个州级补贴已关闭，NSW 仅保留 VPP 激励，SA 的 VPP 补贴最高 $2,050。趋势是"联邦补贴兜底 + VPP 收入驱动"。App 需要向用户清晰展示"联邦补贴节省 + VPP 年化收入"的组合经济账
> - **SAA 认证安装商要求影响渠道策略**：产品必须由 SAA 认证安装商安装才能享受补贴。安装商 B 端工具（Installer Portal）在澳洲市场的重要性不亚于 C 端 App——安装商是实际的渠道决策者。Enphase 的 Installer Toolkit 是对标方向
> - **日装 1,500 套的节奏下，安装商效率工具比 C 端 App 更紧迫**：市场爆发速度远超预期，SAA 认证安装商的排期已成为实际瓶颈。帮助安装商缩短单次安装耗时的工具——标准化调试流程、远程预配置、一键 VPP 激活——将直接决定安装商每日能完成的订单量。这对品牌来说是强渠道黏性，而非边缘体验优化；在安装商选品时，"你们的安装工具让我一天多装 3 台"比"你们的 App 做得好看"更有决策权重
> - **西澳新规 + NEM 多州差异，固件需要维护跨州合规矩阵**：WA 更新 WEM Procedure 要求逆变器默认 grid-interactive，NEM 各州的 VPP 聚合商接口要求不统一——单一固件版本无法覆盖所有市场。固件团队需要建立"州 × VPP 聚合商 × 协议版本"的合规矩阵，并在 App 端通过设备激活流程自动识别用户所在州并推送对应合规配置，避免手动配置错误
> - **澳洲无阳台储能概念，便携储能是户外/应急场景**：澳洲的住宅形态（独栋 house 为主）和电网覆盖决定了阳台储能没有市场基础。便携储能在澳洲更多是 camping/off-grid 场景，走消费电子渠道，与家储是完全不同的销售链路
> - **"被动电池"峰值减负 80% 是重要的 App 叙事锚点——不参与 VPP 的用户同样创造了真实的电网价值**：AEMO 数据表明每套被动家庭电池在峰值时段减负约 1.4 kW（80%），这个数字比任何营销文案都有说服力。App 首屏可展示"今日为电网减负 X kWh"指标（基于 AEMO 公开的峰值时段数据估算），让不参与 VPP 的用户也能感知自己的社会贡献，提升品牌归属感和续费率——而且这不需要 VPP 接入，只需要 App 端的数据可视化能力
> - **AEMC $5,000 万激励 2026-04 已开放，VPP 接口认证应立即排入 2026 Q3 路线图，不能等 2027-05**：$5,000 万早期参与资金已在分配，面向提前接入聚合商平台的资源方（包括家储硬件厂商提供聚合商 API 接入支持）。2027-05 调度模式正式生效后 VPP 聚合商竞价需完成技术合规认证，届时再赶会丧失先发优势。建议：立即接触澳洲主流 VPP 聚合商（Tesla Energy Plan、AGL、Origin、Amber Electric），在 2026 Q3 完成 API 接口认证对接，借助 $5,000 万激励分摊认证和集成成本
> - **SA REPS 补贴实质收紧（非优先群体已无法申请），南澳市场 VPP 销售逻辑需从"补贴驱动"切换为"套利收益驱动"**：VPP1 暂停 + 非优先群体锁定，意味着 SA 普通家庭用户通过 REPS 快速回本的路径基本关闭。App 在南澳市场的 VPP 推广文案需调整：突出"Amber/Tesla/AGL 每年 $300-$1,000 套利收益"而非"最高 $2,050 REPS 补贴"（后者对绝大多数用户已不适用）。**VIC 收入门槛 7 月 1 日降至 $15 万**：App 内的"补贴资格快速查询"功能须在 6 月 30 日前更新门槛逻辑，避免向年收入 $15-21 万的维州用户展示已失效的补贴预期，引发退款投诉
> - **NSW VPP 激励已于 2025-07-01 从证书制切换为前置支付，App 收益展示逻辑需更新**：NSW VPP 激励从旧的"证书额度（$60-$1,680 PREO 证书）"升级为一次性前置支付——10 kWh 电池约 $1,100，上限 $1,500（28 kWh 时触及）。更重要的是：这笔钱在安装时直接从价格中扣减，而非事后返还。App 内的"NSW 收益测算"模块须同步更新：展示"联邦补贴（CHB）+ NSW VPP 前置支付"的组合节省（典型 10 kWh 用户合计超 $4,200），并明确说明 NSW VPP 前置支付与联邦补贴可叠加、且无需事后申请，以提升用户在安装决策时的置信度
> - **CHB 计划一周年累计突破 40 万套 / 11.2 GWh，存量运营价值已超过新增拉新价值——App 应从"促装机"转向"促续费与增值服务"**：计划自 2025-07-01 启动至 2026-06 满一年，累计安装已超 40 万套，平均装机容量翻倍，意味着澳洲家储用户基数已具备规模化运营的门槛。对产品策略的含义：① VPP 收益优化、OTA 固件升级、能源报告等增值服务应成为存量用户 ARPU 提升的核心抓手，而非仅依赖新增装机拉动收入；② 40 万套的用户池足以支撑独立的澳洲本地化客服和运营团队投入产出比；③ 补贴阶梯递减（每半年一次）意味着后续新增用户的补贴强度将持续走低，用户全生命周期价值（LTV）中"软件订阅+服务"的占比会逐年提高，产品定价策略应提前布局订阅制或增值包
> - **NSW 准入容量上限 7-1 起从 28 kWh 扩大至 50 kWh，但激励仍按 28 kWh 封顶——App 需要向大容量用户讲清"资格 vs 收益"的区别，避免预期落差投诉**：PDRS BESS2 允许 28-50 kWh 电池参与激励计划，但补贴金额计算仍以前 28 kWh 可用容量为上限，超出部分不再额外计入。这意味着容量扩大主要是"解锁大容量电池的市场准入资格"而非"提高补贴金额"。产品建议：① App 内 NSW 收益测算模块的容量输入框上限需同步从 28 kWh 调整为 50 kWh，但计算逻辑必须清晰展示"前 28 kWh 计入激励、超出部分不计入"的封顶规则，避免用户误以为大容量电池能拿到更高补贴；② 电池须在 CEC（Clean Energy Council）清单在册才符合 BESS2 资格，App 选品/报价流程中应加入 CEC 清单校验节点，防止安装商向客户推荐不合规 SKU

---

## 附：关键跟踪源

完整信息源目录见 → [储能行业信息源汇总](../reference_sources.md)

| 类别 | 核心信息源 |
|------|-----------|
| **行业新闻** | Energy-Storage.News、ESS News、PV Magazine（含德语/澳洲版）、CleanTechnica |
| **政策监管** | European Commission Energy、KfW、BAFA、GSE、Ofgem、Clean Energy Regulator |
| **行业协会** | Energy Storage Europe（原 EASE）、BVES、SolarPower Europe、Clean Energy Council |
| **德语社区** | Photovoltaikforum、Solaranlagen Forum、Energiemagazin |
| **澳洲平台** | SolarQuotes、One Step Off The Grid、Energy Matters、Solar Choice |
| **行业报告** | BNEF、Wood Mackenzie、SolarPower Europe 年报 |
