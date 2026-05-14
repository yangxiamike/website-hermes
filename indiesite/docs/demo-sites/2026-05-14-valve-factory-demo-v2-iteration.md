# 阀门工厂 Demo V2 迭代记录：去 AI 味

日期：2026-05-14
阶段：产品制作阶段
资产：Valve Factory Demo Site V2
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo
负责人：Hermes
协作角色：Mira / Dex / Nora

---

## 1. 触发原因

创始人反馈：第一版 demo “AI 味浓浓的”。

判断成立。V1 的问题不是方向错，而是表达方式太像 AI 生成的 SaaS/模板站：

- Hero 渐变、玻璃卡片、圆角阴影过重
- CSS 抽象阀门图像太像占位插画
- 文案在解释“网站怎么帮助买家”，而不是阀门工厂对采购说话
- 大量 buyer-focused / trust signals / generic slogans / demo 等自我解释词
- 产品、质检、包装、文件、标准等采购细节不够密

---

## 2. V2 改造原则

### 2.1 文案原则

从“服务商解释网站”改成“工厂对采购说话”。

删除或弱化：

- buyer-focused
- trust signals
- generic slogans
- demanding applications
- demo site
- we help buyers
- reliable / professional / solution 等泛词

增加：

- valve type
- size
- pressure class
- material
- seat / seal
- medium
- temperature
- end connection
- test standard
- MTC
- pressure test report
- packing photos
- destination port

### 2.2 视觉原则

从“漂亮模板站”改成“克制工业资料站”。

改动：

- 去掉深蓝渐变 hero
- 去掉玻璃卡片、过度阴影、hover 上浮
- 降低圆角和营销感
- 增加 topbar 工业信息条
- 增加 RFQ checklist、规格表、QC 表、流程表
- 使用工程资料感的线框阀门示意，不使用未经授权真实素材

---

## 3. 已完成改动

### 页面

已重写：

1. index.html
2. products.html
3. ball-valve.html
4. factory.html
5. quality.html
6. assets/styles.css

V1 已备份到：

/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/_archive

### 首页变化

- H1 改为：Industrial valves for OEM buyers, contractors, and project distributors
- 首屏改为 RFQ checklist，不再使用泛营销大图
- 产品区改为按 type / material / pressure class / end connection 展开
- 应用区增加 medium / pressure / temperature / corrosion risk 等真实采购判断
- 工厂区改为 technical review → machining & assembly → testing & packing
- RFQ 表单增加具体询盘示例

### 产品页变化

- Ball Valve 页面重写为规格导向页面
- 增加 configuration options
- 增加 inspection before shipment
- 增加更完整的 specification table：design standard、face to face、flange standard、test standard、marking、packing 等

### Factory / Quality 页面变化

- 增加 export packing check
- 增加 order control points
- 增加 QC stage table
- 增加 document request 说明

---

## 4. 自检结果

链接与基础 SEO 检查：通过

- HTML 页面数：5
- CSS 文件：1
- title：全部存在
- meta description：全部存在
- viewport：全部存在
- 内部链接：通过
- index.html#rfq anchor：通过
- mobile media query：存在
- AI 味高风险词检查：通过

本地 HTTP 服务检查：通过

- index.html：200
- products.html：200
- ball-valve.html：200
- factory.html：200
- quality.html：200
- assets/styles.css：200

---

## 5. Nora QA

结果：Conditional Pass，明显优于 V1。

### 已解决

- P0：没有伪装真实客户案例
- P0：没有虚构真实证书、真实客户、真实项目
- P0：没有未授权真实素材
- P0：基础可访问性和链接无严重问题
- P1：AI 模板感已显著下降
- P1：文案从抽象服务商话术改为采购/工厂语言

### 仍需改进

P1：视觉仍是静态工程感，还缺少高质量工业素材或更高级的信息图。

P1：品牌 Northvale Flow Control 仍偏国际化，不完全像中国出口工厂升级后的品牌。

P2：还缺 before / after 改造说明页，无法直接展示“我们改造了什么”。

P2：移动端仅做了基础响应式，没有做逐屏视觉验收。

---

## 6. 当前状态

V2 可以作为内部评审版本继续看方向。

相比 V1，已经从“AI 生成的漂亮工业模板”推进到“更像真实阀门出口工厂资料站”。

但距离“可放进公司官网案例库的展示资产”还差一轮：

1. 增加 before / after 案例包装
2. 增加更真实的工业视觉资产
3. 微调品牌气质，让它更像中国出口工厂英文站升级版
4. 做移动端逐屏 QA
