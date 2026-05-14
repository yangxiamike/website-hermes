# 阀门工厂旧站改造 Before / After 案例页制作记录

日期：2026-05-14
阶段：产品制作阶段
资产：Old Valve Website Renovation Case / Before & After Comparison
负责人：Hermes / Mira / Dex / Nora
路径：/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/before-after.html

---

## 1. 资产目标

基于当前阀门工厂 Demo，制作一个可放入公司官网或服务介绍页的旧站改造案例资产，用来说明：

- 旧英文站为什么不能建立海外买家信任
- 改造后的网站如何围绕采购决策组织信息
- 我们的服务不是普通美化，而是把真实制造能力翻译成买家能判断的页面结构

该页面目前作为内部展示资产，不代表真实客户案例。

---

## 2. 页面内容结构

新增页面：`before-after.html`

页面结构：

1. Hero：说明这是旧站改造 before/after sample case
2. Old site diagnosis：列出旧站常见问题
   - 产品页只是分类列表
   - 没有制造能力证明
   - 没有清晰 RFQ 路径
3. Visual before/after：用简单页面模型对比旧站和升级站
4. Upgrade map：用表格说明首页、产品页、工厂能力、QC、询盘路径的改造差异
5. Trust expression：解释升级后的表达为什么更像真实出口工厂
6. Case takeaway：说明该案例可用于服务官网包装

---

## 3. 内容原则

Mira 侧重点：

- 避免空泛 web design 话术
- 使用海外采购会真正检查的字段：valve type、size、pressure class、material、seat、connection、medium、temperature、MTC、test report、packing list
- 不承诺排名、询盘或订单结果
- 不使用真实客户名称、logo、证书或项目数据

Dex 侧重点：

- 复用当前阀门 Demo 的视觉系统和 CSS
- 增加 before/after 专用视觉模块
- 页面具备 title、meta description、viewport、CSS 引用
- 更新 Demo 站导航和 README，让案例页可被访问

Nora 侧重点：

- 页面要能解释服务价值，但不能像虚假真实案例
- fictional/sample disclosure 必须清楚
- 对外公开前仍需创始人确认

---

## 4. 已修改文件

- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/before-after.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/assets/styles.css`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/index.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/products.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/ball-valve.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/factory.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/quality.html`
- `/Users/ml/Documents/New project/indiesite/demo-sites/valve-factory-demo/README.md`

---

## 5. 验证结果

本轮已完成：

- 6 个 HTML 页面 metadata 检查通过
- CSS 文件存在并加载路径正确
- 内部链接和 anchor 检查通过
- 移动端 media query 存在
- 本地 HTTP 访问 200：
  - index.html
  - products.html
  - ball-valve.html
  - factory.html
  - quality.html
  - before-after.html
  - assets/styles.css

---

## 6. 展示状态

当前状态：内部展示可用，Nora 结论为 Conditional Pass。

可作为公司官网“旧站改造案例”模块的第一版素材，但公开前建议再做一轮视觉精修，加入更强的 industrial document 风格元素，例如：

- 旧站诊断报告卡片
- 改造后 RFQ 表格截图式模块
- QC report / packing label / nameplate mockup
- 中文内部注释版案例包装
