<!-- ELUCENIA technical documentation · ariscat · zh · no clinical/professional/rights approval -->

# ARISCAT

[条件、来源与许可](https://elucenia.org/zh/tools/ariscat)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 年龄

`idade`

- `0` — ≤ 50 岁
- `3` — 51 至 80 岁
- `16` — \> 80 岁

### 术前氧饱和度（静息、空气吸入）

`sat`

- `0` — ≥ 96%
- `8` — 91 至 95%
- `24` — ≤ 90%

### 过去一个月有呼吸道感染

`infec`

### 术前贫血（Hb ≤ 10 g/dL）

`anemia`

### 切口部位

`incisao`

- `0` — 外周
- `15` — 上腹部
- `24` — 胸腔内

### 手术时长

`duracao`

- `0` — ≤ 2 h
- `16` — \> 2 h且≤ 3 h
- `23` — \> 3 h

### 急诊手术

`emerg`

## 方法版本

ARISCAT/Canet 2010，表6：7个加权因素；时长≤ 2 h = 0，\> 2 h且≤ 3 h = 16，\> 3 h = 23

## 已记录的公式

年龄51–80岁 = 3，\> 80岁 = 16 · SpO₂ 91–95% = 8，≤ 90% = 24 · 过去1个月内呼吸道感染 = 17 · Hb ≤ 10 g/dL = 11 · 上腹部切口 = 15，胸腔内切口 = 24 · 时长≤ 2 h = 0，\> 2 h且≤ 3 h = 16，\> 3 h = 23 · 急诊手术 = 8。

## 限制与适用人群

ARISCAT 2010在59家医院2464名接受全身、椎管内或区域麻醉的手术患者队列中建立并验证，结局为术后肺部并发症。本次阅读的摘要未提供最低年龄、排除条件以及完整权重和分档；队列发生率并非为其他人群重新校准的个体估计。 新近阅读2010年原始论文后，方法部分确认对象为至少18岁的成人，并规定该队列的排除条件；表6确认时长≤2 h、\>2至≤3 h和\>3 h。高风险分界在表7为≥45，而正文为\>45；此处尚未裁定这一文献内部差异。

## 参考文献

- [Canet J et al. Prediction of postoperative pulmonary complications in a population-based surgical cohort. Anesthesiology, 2010.](https://doi.org/10.1097/ALN.0b013e3181fc6e0a)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
