# 阀门工厂 Demo V3 迭代记录：增强真实工业质感

日期：2026-05-14
资产：Valve Factory Demo Site
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo
任务来源：Kanban t_28efebd6

---

## 1. 本轮目标

根据 QA P1-1，增强阀门工厂 Demo 的真实工业质感，重点补齐：

- 产品视觉
- 工厂场景
- 检测流程
- 包装发货场景

约束：不使用未经授权真实客户素材、真实工厂照片、真实证书或真实品牌资料。优先使用自制示意图。

---

## 2. 完成改动

### 2.1 首页

在首屏后新增工业视觉证据条：

- Product / flanged ball valve
- Shop floor / machining
- QC / pressure test
- Export packing

每个视觉块都明确是 demo 自制示意，不伪装成真实客户照片。

### 2.2 Products 页面

在产品表格前新增产品范围视觉条，强化产品、检测、包装和车间能力之间的关系。

### 2.3 Ball Valve 页面

新增产品视觉区域和 Photo Set To Request 清单，用于说明真实客户项目中应向工厂收集哪些授权图片：

- 产品正面 / 侧面 / 法兰面 / 手柄或执行器
- 铭牌与规格信息
- 压力测试照片
- 包装与装柜照片

### 2.4 Factory 页面

新增 Workshop Scenes 模块，用自制示意图表达：

- Machining bay
- Hydrostatic test
- Packing area

### 2.5 Quality 页面

新增 Inspection Evidence 流程块：

- Material check
- Dimensional check
- Pressure test
- Packing check

文案从“质量承诺”转向“订单记录与可索取文件”。

### 2.6 CSS

新增一组自制工业示意图样式：

- .visual
- .v-valve
- .v-factory
- .v-test
- .v-pack
- .evidence-strip
- .photo-panel
- .shop-scenes
- .qc-flow

全部为 CSS 生成的示意图，不依赖外部图片。

---

## 3. 自检结果

通过：

- HTML 页面：6 个
- 内部链接：通过
- index.html#rfq anchor：通过
- title / description / viewport：通过
- CSS：可访问
- 本地 HTTP 服务：通过

本地检查地址：

- /
- /products.html
- /ball-valve.html
- /factory.html
- /quality.html
- /before-after.html
- /assets/styles.css

全部返回 200。

---

## 4. Nora 判断

结果：Conditional Pass

本轮解决了 P1-1 的核心问题：视觉不再只是表格和抽象版式，已经加入产品、车间、测试和包装四类工业场景。由于仍是 CSS 自制示意图，不等同于真实工业摄影质感；但它符合当前阶段“展示信息架构与资产方向”的要求，且没有素材版权风险。

后续若进入对外案例库，应继续替换或补充：

- 可商用工业照片
- 自制 3D/矢量产品渲染
- 更真实的包装、铭牌、压力表、测试台细节

---

## 5. 当前状态

V3 可作为内部展示资产继续进入下一轮评审。公开前仍建议做移动端逐屏截图 QA 和视觉精修。
