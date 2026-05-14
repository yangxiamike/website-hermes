# 阀门工厂 Demo V2 QA 记录

日期：2026-05-14
阶段：产品制作阶段
资产：Valve Factory Demo Site V2
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo
审核角色：Nora

---

## QA 结论

结果：Conditional Pass

V2 已经明显降低 V1 的 AI 味，当前适合继续作为内部评审版本。暂不建议直接公开发布。

---

## 已通过项

- 5 个页面均可访问
- CSS 正常加载
- 内部链接和 RFQ anchor 通过
- 每页具备 title / meta description / viewport
- 有移动端 media query
- 删除了明显的服务商解释型文案
- 删除了 buyer-focused / trust signals / generic slogans 等 AI 味高风险词
- 文案转向采购语言：size、pressure class、material、seat、medium、temperature、test report、MTC、packing photos 等
- 没有伪造真实客户、真实证书、真实项目或真实数据
- 没有使用未授权真实素材
- 页脚保留了 internal sample / fictional manufacturer 风险提示

---

## P0

无。

---

## P1

1. 视觉仍然偏静态资料站，需要下一轮提高审美完成度。
2. 品牌名 Northvale Flow Control 偏国际化，不完全像中国出口工厂升级后的英文站。
3. 产品和工厂页面还可以加入更真实的信息图：铭牌、测试报告样张、包装标签、RFQ 表格等。
4. 移动端只做基础响应式，尚未逐屏验收。

---

## P2

1. 增加 before / after 页面，用来展示旧站改造价值。
2. 增加中文内部案例包装页，解释这个 demo 如何体现服务能力。
3. 建立术语表，统一 valve / pressure / material / testing / packing 表达。
4. 后续可加入可商用或自制视觉素材。

---

## 当前建议

进入 V3：案例包装 + 视觉资产增强。

V3 目标不是再堆页面，而是让它能成为公司官网上的第一个展示案例。
