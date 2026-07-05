# Tibber VPP 计划与家储设备调度权分析

> 最后更新：2026-07-05
> 分析范围：Tibber Grid Rewards / VPP 协议条款、调度机制、设备兼容性、厂商策略

---

## 一、Tibber VPP 概述

Tibber 通过其 **Grid Rewards** 服务构建了欧洲最大的居民侧虚拟电厂（VPP），将用户的家庭电池、EV 充电桩、电动车等设备聚合为统一的可调度资源池，代替传统电厂参与电网频率调节（FCR/FRR）和平衡市场。电网运营商为此向 Tibber 付费，Tibber 再将部分收益分配给用户。

**当前覆盖市场：** 瑞典、荷兰（已上线），德国及其他欧洲市场（扩展中）

---

## 二、调度机制拆解

### 2.1 技术架构

Tibber 通过云端 API 下发调度指令，而非物理接线控制，技术链路如下：

```
Tibber 云平台 → Enode 中间件（统一 API 层）→ 设备厂商云 → 逆变器/BMS → 电池
```

Tibber 能调度一块电池的前提条件：

1. 电池/逆变器厂商已开放云端 API
2. 该 API 已被 Enode 或 Tibber 直接对接
3. 用户在 Tibber App 中完成 OAuth 授权，将设备账号与 Tibber 关联

### 2.2 Homevolt 运行模式

Tibber 自家电池 Homevolt 提供两种运行模式，用户在 App 中自行切换：

| 维度 | Earnings Mode（收益优先） | Self-Consumption Mode（自用优先） |
|------|--------------------------|----------------------------------|
| **充放电策略** | Tibber 根据市场信号自动买低卖高，参与 FCR/FRR 平衡市场 | 优先消纳自家光伏，最小化电网交互 |
| **Grid Rewards 参与度** | 完全参与，电池纳入 VPP 统一调度池 | 有限参与，基本不参与电网平衡 |
| **调度主体** | Tibber 平台（自动扫描市场、预判需求、响应价格信号） | 本地优先，仅在价格最优时段释放光伏电量 |
| **用户控制权** | 让渡给 Tibber 算法 | 保留在本地策略 |

Tibber 官方建议用户选择 Earnings Mode，理由是 Self-Consumption Mode "不会产生显著收益"。本质上是在引导用户将调度权交给平台。

### 2.3 EV 充电桩的 VPP 参与

EV 充电桩无需家庭电池即可独立参与 Grid Rewards：

- Smart Charging 自动在低价时段充电
- Grid Rewards 在此基础上增加电网平衡响应——高峰时暂停充电，低谷时加速充电
- 用户不会因调度而多付电费（仍按低价时段价格计费），并额外获得 Grid Rewards 补偿
- VPP 响应速度可达秒级/毫秒级

---

## 三、协议条款分析

以 **Tibber × sonnen VPP 协议（瑞典市场）** 为例：

### 3.1 远程控制权（条款 5.1）

> Tibber will **remotely access and operate** your sonnenBatterie, including to **charge or discharge** your sonnenBatterie, or **maintain a state of charge at any time**.

Tibber 有权在任何时间远程访问并操作用户电池，包括充电、放电或维持特定 SoC。

!!! warning "条款风险"
    这是一条非常宽泛的授权——没有限定调度频次上限、没有明确 SoC 保底值、没有约定单次调度时长。

### 3.2 补偿结构（条款 4.1-4.2）

- 按月度积分（Tillgodo/Monthly Credit）发放
- 计算依据：电池可用天数 × 电池功率（kW）
- 积分与 Tibber 账单一同发送，正余额可在 2 个月内转账至银行账户
- **条款 4.1 明确声明：不承诺任何财务收益**

### 3.3 合同期限与退出（条款 3.2-3.3, 8.2）

| 条款 | 内容 |
|------|------|
| 最短期限 | 1 个月 |
| 续约方式 | 自动按月续约 |
| 用户退出 | 随时可通过在线表单或邮件申请取消 |
| 冷静期 | 14 天无理由撤销权 |
| Tibber 终止 | 需提前 30 天书面通知 |

### 3.4 责任限制

- 赔偿上限为过去 6 个月积分总额
- 不对利润损失、数据丢失或间接损害负责
- 允许采集电池使用数据用于"商业目的"，授权范围较宽

### 3.5 与行业标杆的对比

| 维度 | 行业通行做法 | Tibber 条款 | 评价 |
|------|-------------|-------------|------|
| SoC 保底 | 用户可设 20-30% SoC floor，合同约束 | 未明确约定 | ⚠️ 偏弱 |
| 调度频次 | 50-100 次/年上限 | 未明确约定 | ⚠️ 偏弱 |
| 等效循环 | 全年新增 <10 个等效满循环 | 未明确约定 | ⚠️ 偏弱 |
| 单次调度时长 | 5-15 分钟，2-5 kWh | 未明确约定 | ⚠️ 偏弱 |
| 用户 override | 如 Amber SmartShift 允许实时覆盖 | 可切换模式，但无实时 override | 一般 |
| 退出机制 | 随时退出 | 随时退出 | ✅ 对齐 |

---

## 四、设备兼容性与未支持电池场景

### 4.1 当前支持的第三方电池品牌

| 品牌 | 接入状态 | 备注 |
|------|---------|------|
| Tibber Homevolt | ✅ 已上线 | 自有品牌，深度集成 |
| sonnen | ✅ 已上线 | 独立合作条款（sonnenVPP） |
| Huawei（LUNA2000） | ✅ 已上线 | 通过 Enode 集成 |
| KOSTAL | ✅ 已上线 | Grid Rewards 支持 |
| SolaX | ✅ 已上线 | Grid Rewards 支持 |
| SAJ | ✅ 已上线 | Grid Rewards 支持 |
| Sigenergy | 🔄 合作签约 | 集成中 |
| Sungrow | 🔄 合作签约 | 集成中 |
| GoodWe | 🔄 合作签约 | 集成中 |

### 4.2 未支持电池的用户场景

当用户的家庭电池不在 Tibber VPP 支持列表中，但用户通过 EV 充电桩等其他设备加入了 VPP 协议：

| 场景 | 实际表现 |
|------|---------|
| 用户通过 EV 充电桩加入 VPP | 充电桩正常参与调度，电池无感知 |
| 用户在 Tibber App 尝试关联电池 | 设备列表中找不到该品牌，无法绑定 |
| 电池日常运行 | 按自身逆变器/EMS 的本地策略运行，与 Tibber 完全独立 |
| Grid Rewards 调度事件发生 | Tibber 只调度充电桩/EV，电池不响应也不获得补偿 |
| 电网高峰需要放电 | 电池可能在自用模式下放电（巧合一致），但不受 Tibber 指挥 |

**核心结论：没有 API 通道 = 没有调度权 = 电池是 VPP 网络中的"盲区"。**

### 4.3 调度策略冲突风险

两套独立策略可能产生冲突：

**冲突场景 1：电网高峰期**

```
Tibber VPP 策略：暂停 EV 充电桩充电（减少负荷）
电池本地策略：检测到高电价，自动放电供家庭使用（减少购电）

结果：
- 充电桩停了 → EV 没充上电
- 电池放了 → 家庭负荷下降
- Tibber 不知道电池放了电，调度模型预测与实际偏差变大
```

**冲突场景 2：电网低谷期**

```
Tibber VPP 策略：给 EV 大功率充电（消纳多余电力）
电池本地策略：也在低价时段充电

结果：
- 家庭总功率可能超过入户线容量限制
- 两个设备抢电，都充不满
```

### 4.4 对用户的影响

- **认知错位**：用户看到"已加入虚拟电厂"，容易误以为所有储能设备都在参与，实际只有充电桩在工作
- **收益低于预期**：电池容量未被纳入调度池，Grid Rewards 补偿仅基于充电桩的灵活性
- **设备协调缺失**：充电桩与电池各行其是，无法实现全屋能源最优解

---

## 五、对储能厂商的战略启示

### 5.1 不接入 = 被边缘化

Tibber 在欧洲已经是最大的居民侧 VPP（百万级设备接入）。电池不在支持列表中意味着：

- 用户选购时被 Tibber App 的"兼容设备推荐"引导至竞品
- 安装商为减少后续服务成本，优先推荐已认证设备
- VPP 兼容性正在从"加分项"变成"入场券"

### 5.2 接入 = 需要保护自身利益

一旦开放 API 给 Enode/Tibber，电池可被第三方远程充放电。从 Tibber 条款来看，聚合商要的权限很宽，对电池寿命的保护条款几乎没有。厂商需要在 API 层面做好自我保护，而非依赖聚合商的合同条款。

### 5.3 建议策略

**短期（防守）——API 层做好护栏**

- 开放 API 给 Enode/Tibber，但在固件层硬编码保护参数：
    - SoC floor（如 20%）
    - 单日最大调度次数
    - 最大等效循环数
- 这些限制写在 BMS 里，上层聚合商无法突破
- 对用户透明：App 里可查看"VPP 今日已调度 X 次，剩余配额 Y 次"

**中期（卡位）——争取聚合商优先合作伙伴**

- 与 Tibber 等聚合商签订设备级 SLA（而非只让用户签 VPP 协议）
- 在合作协议中约定：调度频次上限、循环寿命补偿机制、电池损耗分摊
- 作为交换，给聚合商更深度的 API 权限（如实时 SoH 数据）

**长期（进攻）——自建 VPP 能力**

- 自己做聚合商，或为安装商提供白标 VPP 平台
- 把 VPP 收益留在自己的生态里，而非被第三方抽成
- 利用对 BMS 数据的天然优势，做出比 Tibber 更精准的调度策略

---

## 六、厂商接入 Tibber VPP 的 API 能力要求

### 6.1 Tibber 的接入架构：不直连厂商，通过 Enode 中间层

Tibber 并不直接对接每个电池厂商的 API，而是通过 **Enode**（能源设备统一 API 中间件）作为集成层。厂商要进入 Tibber VPP 的支持列表，实际上是要先被 Enode 平台集成。

```
电池厂商云 API ← Enode 集成 ← Tibber 调用 Enode 统一 API ← Tibber VPP 调度引擎
```

因此，**Tibber 自身没有公开发布一份面向电池厂商的 API 接入规范文档**。厂商需要满足的是 Enode 的集成要求，而 Enode 的要求又反映了聚合商（包括 Tibber）对电池的调度需求。

### 6.2 Enode 对电池厂商 API 的接入要求

Enode 官方的合作门槛描述如下：

> "Send us your API documentation. If it supports the key functionality we need and **user access (OAuth is our go-to)**, we're ready to roll."

接入流程分三步：

1. **提交 API 文档** — 厂商将自家云端 API 文档提交给 Enode
2. **Enode 完成集成** — Enode 团队将设备接入其统一平台
3. **上线发布** — 设备型号在 Enode 平台生效，所有使用 Enode 的能源 App（包括 Tibber）均可调用

**核心要求：**

| 要求 | 说明 |
|------|------|
| 云端 API | 厂商必须有可被外部调用的云 API（非本地 Modbus/CAN） |
| OAuth 2.0 授权 | 用户在 Tibber App 中通过 OAuth 授权 Enode 访问自己的设备账号 |
| API 文档完整 | 需涵盖设备发现、状态读取、控制指令等能力 |

### 6.3 Enode 归一化后的电池数据模型（即 Tibber 实际消费的字段）

Enode 将所有厂商的 API 归一化为统一的电池数据模型，以下是 Tibber 等聚合商实际能获取和控制的全部字段：

#### 设备信息（Information）

| 字段 | 类型 | 说明 |
|------|------|------|
| `id` | string | 电池在厂商系统中的 ID |
| `brand` | string | OEM 品牌名称 |
| `model` | string | 电池型号 |
| `siteName` | string | 用户自定义的站点名称 |
| `installationDate` | datetime | 安装日期 |
| `batteryCapacity` | number (kWh) | 电池标称容量 |

#### 充放电状态（Charge State）— 实时遥测

| 字段 | 类型 | 说明 |
|------|------|------|
| `status` | enum | 当前功率状态：`CHARGING` / `DISCHARGING` / `IDLE` / `FAULT` / `UNKNOWN` |
| `chargeRate` | number (kW) | 当前充放电功率，正值=充电 |
| `batteryLevel` | number (%) | 当前 SoC 百分比 |
| `dischargeLimit` | number (%) | 放电下限（SoC floor） |
| `lastUpdated` | datetime | 最后一次数据更新时间戳 |

#### 运行模式控制（Configuration）

| 字段 | 类型 | 说明 |
|------|------|------|
| `operationMode` | enum | 当前运行模式（见下表） |
| `lastUpdated` | datetime | 最后一次配置更新时间戳 |

**可设定的运行模式（`operationMode` 枚举值）：**

| 模式 | 含义 | VPP 场景用途 |
|------|------|-------------|
| `SELF_RELIANCE` | 最小化电网依赖，优先自消费 | 退出 VPP 调度时设置 |
| `TIME_OF_USE` | 按分时电价优化充放电 | 配合电价信号调度 |
| `IMPORT_FOCUS` | 优先充电（从电网或光伏） | 电网低谷消纳 |
| `EXPORT_FOCUS` | 优先放电到家庭/电网 | 电网高峰响应 |
| `IDLE` | 禁止充放电，维持当前 SoC | 暂停调度 |

#### 位置信息（Location）

| 字段 | 类型 | 说明 |
|------|------|------|
| `longitude` | number | 经度 |
| `latitude` | number | 纬度 |

#### 能力声明（Capabilities）

每块电池通过 `capabilities` 对象声明自己支持哪些模式，每个能力项包含 `isCapable` 布尔值。聚合商据此判断能否下发特定控制指令。

### 6.4 Enode 提供的控制指令（API Endpoints）

| 端点 | 方法 | 功能 |
|------|------|------|
| `/batteries` | GET | 列出所有已关联电池 |
| `/batteries/{batteryId}` | GET | 获取单个电池详情 |
| `/users/{userId}/batteries` | GET | 获取用户名下所有电池 |
| `/batteries/{batteryId}/operation-mode` | POST | **设置运行模式**（核心调度指令） |
| `/batteries/actions/{actionId}` | GET | 跟踪指令执行状态 |
| `/batteries/{batteryId}/action/{actionId}/cancel` | POST | 取消待执行指令 |
| `/batteries/{batteryId}/refresh-hint` | POST | 请求立即刷新数据 |

**指令执行状态机：**

```
PENDING → CONFIRMED（成功）
        → FAILED（失败：NO_RESPONSE / FAILED_PRECONDITION / NOT_FOUND）
        → CANCELLED（被取消）
```

**权限作用域（Scopes）：**

| Scope | 权限 |
|-------|------|
| `battery:read:data` | 读取电池状态数据 |
| `battery:read:location` | 读取地理位置 |
| `battery:control:operation_mode` | 控制运行模式 |

### 6.5 HEM System（Home Energy Management 统一数据层）

Enode 还提供 HEM System API（beta），将同一站点的逆变器、电池、电表统一为一个系统对象，提供：

- 光伏发电量（solar generation）
- 家庭用电量（household consumption）
- 电网进出口（grid import/export）
- 电池充放电（battery charge/discharge）
- 时间序列数据，分辨率 5-15 分钟（因厂商而异）

**已支持 HEM System 的电池品牌（API 版本 2024-10-01+）：**

Enphase、FoxESS、GivEnergy、Huawei、SMA、SolarEdge、SolaX、Solis、Tesla

### 6.6 行业通用标准对比

Enode 的云 API 路线并非唯一选择。行业中还有多种 VPP 集成标准：

| 标准/协议 | 层级 | 典型场景 | 与 Enode 路线的关系 |
|-----------|------|---------|-------------------|
| **SunSpec Modbus** | 本地通信 | 逆变器/电池本地监控与控制 | Enode 在厂商云端间接消费这些数据 |
| **IEEE 2030.5** | 设备到聚合商 | 美国/澳洲 DER 管理（Rule 21、AS4777.2） | 更偏电网侧合规，Enode 暂未依赖 |
| **OpenADR 2.0b/3.0** | 聚合商到电网 | 需求响应事件信号 | Tibber 作为聚合商对接电网，与厂商 API 无关 |
| **OCPP** | 充电桩通信 | EV 充电桩 VPP 集成 | 仅适用于充电桩，不涉及家储 |
| **厂商私有云 API** | 云到云 | Enode 当前采用的主要路线 | 最快落地，但依赖厂商开放度 |

### 6.7 厂商 API 开放的关键决策点

!!! warning "核心矛盾"
    Tibber/Enode 对电池的控制粒度是**模式级**（切换运行模式），而非**功率级**（设定精确的充放电功率值）。这意味着聚合商只能告诉电池"现在进入放电模式"，但不能指定"以 2.5kW 放电 15 分钟"。

这带来两个推论：

**1. 当前 Enode 模式对 FCR/FRR 等精细化电网服务支持有限**

FCR 要求亚秒级响应和精确功率控制，而 Enode 的模式切换 API 做不到这个精度。Tibber 参与 FCR 时，大概率是通过以下方式之一：

- 对 Homevolt 自家电池走本地 API（支持 power limits、PID 控制）
- 对第三方电池仅参与门槛较低的 mFRR（12.5 分钟响应）或容量市场

**2. 厂商如果只开放模式切换，调度价值有上限**

如果厂商想让自己的电池在 VPP 中获得更高的调度优先级和补偿，需要考虑开放更细粒度的 API：

| 能力层级 | 开放内容 | 可参与的市场 | 补偿潜力 |
|---------|---------|------------|---------|
| **L1：状态只读** | SoC、功率、容量 | 无法调度，仅监控 | 无 |
| **L2：模式切换** | 运行模式切换（Enode 当前水平） | mFRR、容量市场、电价套利 | 中 |
| **L3：功率设定** | 精确充放电功率（kW）+ 时长 | aFRR、能量套利 | 高 |
| **L4：实时调频** | 毫秒级功率响应 + PID 控制 | FCR | 最高 |

**大多数第三方电池目前停留在 L2 水平（通过 Enode），而 Tibber 自家的 Homevolt 可以做到 L3-L4。这就是 Tibber 推自家硬件的根本动机之一——不是因为第三方电池不好，而是第三方的 API 开放深度不够。**

---

## 七、关键结论

| 问题 | 结论 |
|------|------|
| 加入 VPP 后电池是否归 Tibber 调度？ | **是**，选择 Earnings Mode 后完全由 Tibber 算法统一调度 |
| 协议是否有明确规定？ | **有**，条款 5.1 明确授权远程充放电控制，权限范围很宽 |
| 用户能否退出？ | **可以**，随时切换模式或终止合约 |
| 协议对用户保护是否充分？ | **偏弱**，缺少 SoC 保底、调度频次上限、电池寿命保障等行业通行条款 |
| 电池未被支持时会怎样？ | 电池不被调度、不获补偿，成为 VPP 网络盲区，且可能与充电桩策略冲突 |
| 厂商是否应该接入？ | **应该**，但需在固件层做好保护，不能依赖聚合商条款 |
| Tibber 是否规定了厂商 API 的开放要求？ | **没有直接规定**。Tibber 通过 Enode 中间层接入，厂商需满足 Enode 的要求：云端 API + OAuth 2.0 + 至少支持模式切换 |
| API 开放到什么深度最合适？ | 当前 Enode 水平为 L2（模式切换），但要获得更高调度优先级和补偿，需向 L3（功率设定）演进。L4（实时调频）是 Tibber 推自家 Homevolt 的核心壁垒 |

---

## 参考来源

- [Tibber × sonnen VPP 条款（瑞典）](https://tibber.com/se/partner/sonnen/villkor)
- [Tibber Grid Rewards 官方页面](https://tibber.com/en/grid-rewards)
- [Grid Rewards Q&A](https://tibber.com/en/magazine/inside-tibber/what-is-grid-rewards)
- [Homevolt 能源优化模式详解](https://tibber.com/en/magazine/power-hacks/how-homevolt-optimizes-energy)
- [VPP 如何释放分布式能源的力量](https://tibber.com/en/magazine/inside-tibber/drive-energy-independence)
- [Smart Charging + Grid Rewards](https://tibber.com/en/magazine/inside-tibber/smart-charging-plus-grid-rewards)
- [Tibber VPP 上线新闻（ESS News）](https://www.ess-news.com/2024/12/18/tibber-home-battery-grid-rewards-scheme-compensation-homevolt-home/)
- [Tibber 全球条款页](https://tibber.com/en/terms/global)
- [Enode 统一能源设备 API 平台](https://enode.com/)
- [Enode VPP 解决方案](https://enode.com/use-cases/virtual-power-plants)
- [Enode 家庭电池集成](https://enode.com/use-cases/home-batteries)
- [Tibber 与 Enode 合作构建开放能源生态](https://enode.com/blog/customers/from-connected-customers-to-flexible-homes-how-tibber-and-enode-are-shaping-the-open-energy-ecosystem-for-the-next-grid)
- [VPP 合约条款指南（Solar Choice）](https://www.solarchoice.net.au/vpp/contract-terms-conditions-guide)
- [VPP 运作原理 2026（SurgePV）](https://www.surgepv.com/hub/energy-storage/virtual-power-plants)
- [VPP 设备兼容性讨论（DIY Solar Forum）](https://diysolarforum.com/threads/virtual-power-plant-vpp-compatibility.52039/)
- [Enode API Reference](https://developers.enode.com/api/reference)
- [Enode HEM System 公告](https://developers.enode.com/api/changelog/updates/2025-10-23-new-unified-api-support-for-solar-inverters-and-home-batteries-the-hem-system-beta)
- [Enode 硬件合作伙伴计划](https://enode.com/partnership)
- [Enode 设备兼容列表](https://enode.com/connect)
- [Tibber Homevolt 本地 API 文档（GitHub）](https://github.com/tibber/homevolt-local-api-doc)
- [Tibber Developer Portal](https://developer.tibber.com/docs)
- [RMI VP3 — VPP 遥测与计量规范](https://rmi.org/wp-content/uploads/dlm_uploads/2026/03/rmi-march-2026-VP3-Metering-Telemetry-in-Utility-VPPs-Supplement.pdf)
- [SunSpec Modbus 规范](https://sunspec.org/modbus/)
- [VPP 运作原理详解（SurgePV 2026）](https://www.surgepv.com/hub/energy-storage/virtual-power-plants)
