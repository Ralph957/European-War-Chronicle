

# 欧洲战争年鉴 · 可视化

# European War Chronicle · Visualization

**从胡斯战争到一战前 · 1419–1914**



## 📖 项目简介 / Introduction

**中文**
《欧洲战争年鉴》是一个交互式历史可视化项目，涵盖从**胡斯战争（1419年）到第一次世界大战爆发前（1914年）**近500年间的欧洲主要战争与冲突。

项目通过**时空地图 + 动态时间轴**的形式，让用户可以直观探索战争的演变——从宗教战争到王朝争霸，从拿破仑战争到工业战争雏形。点击任意战争，地图将聚焦战场区域，并展示关键战役的详细信息。

*European War Chronicle is an interactive historical visualization project covering nearly 500 years of major European conflicts from the **Hussite Wars (1419)** to the eve of World War I (1914).*

*Through a **spatiotemporal map + dynamic timeline**, users can intuitively explore the evolution of warfare—from religious wars to dynastic struggles, from the Napoleonic Wars to the dawn of industrialized warfare. Click any war to zoom into the battlefield and explore key battles.*



## 📌 项目性质 / Project Nature


这是一个**业余爱好者项目**，而非专业的工程或学术研究项目。作者并非历史学家或专业开发者，制作初衷是结合对历史与可视化技术的兴趣，在学习中构建一个有趣的作品。

本项目将**大量使用 Vibe Coding** 的开发方式，优先追求探索乐趣与个人表达，而非代码的工业级健壮性或数据的全面准确性。

因此，你可能会遇到：

- 数据不完整或存在偏差
- 代码风格不统一
- 功能实现较为随性

如果你也是同好，欢迎一起玩！如果你发现了明显错误，也请温柔地指出。


*This is a **hobbyist project**, not a professional engineering or academic research project. The author is neither a historian nor a professional developer. The motivation is to combine an interest in history with visualization techniques, building something enjoyable through learning.*

*This project will heavily adopt a **Vibe Coding** approach, prioritizing exploration and personal expression over industrial robustness or data completeness.*

*Thus, you may encounter:*

- *Incomplete or biased data*
- *Inconsistent code style*
- *Features implemented in a rather spontaneous manner*

*If you share the same interests, feel free to join the fun! If you spot obvious mistakes, please point them out gently.*



## 🎯 项目目标 / Objectives

| 中文                                         | English                                                      |
| -------------------------------------------- | :----------------------------------------------------------- |
| 将零散的历史战争记录整合为可交互的时空数据集 | Integrate scattered historical war records into an interactive spatiotemporal dataset |
| 帮助用户直观理解战争的地理分布与演变趋势     | Help users intuitively understand the geographic distribution and evolution of warfare |
| 提供分层的信息呈现：宏观→战役→细节           | Provide layered information: macro → battle → detail         |
| 作为历史研究与数据可视化的跨学科实践         | Serve as an interdisciplinary practice of history research and data visualization |



## 🗺️ 核心功能 / Core Features

### 中文

| 功能           | 描述                                                      |
| :------------- | :-------------------------------------------------------- |
| **动态时间轴** | 可拖拽的时间轴滑块，支持按阶段/年份筛选战争               |
| **交互式地图** | 基于 Leaflet/OpenLayers 的欧洲地图，标注战争发生地        |
| **分层详情页** | 点击战争标记 → 地图放大至战场区域 → 显示关键战役点        |
| **战役卡片**   | 每个战役包含：时间、交战方、战术特点、结果（约100-200字） |
| **战争对比**   | 不同战争的兵力、持续时间、地理范围的可视化对比            |
| **中英文双语** | 界面与内容支持中英文切换                                  |

### English

| Feature                 | Description                                                  |
| :---------------------- | :----------------------------------------------------------- |
| **Dynamic Timeline**    | Draggable timeline slider for filtering by period/year       |
| **Interactive Map**     | Europe map (Leaflet/OpenLayers) with war markers             |
| **Layered Detail View** | Click war marker → zoom to region → show key battle points   |
| **Battle Cards**        | Each battle includes: date, belligerents, tactical features, outcome (~100-200 words) |
| **War Comparison**      | Visual comparison of troop sizes, duration, and geographic scope |
| **Bilingual Support**   | Chinese/English toggle for interface and content             |



## 🗂️ 数据范围 / Data Scope

### 五阶段划分 / Five-Stage Division

| 阶段 / Stage                         | 时间范围 / Period |
| :----------------------------------- | :---------------- |
| 晚期中世纪 / Late Medieval           | 1419–1494         |
| 宗教战争时代 / Age of Religious Wars | 1494–1648         |
| 君主专制时代 / Age of Absolutism     | 1648–1789         |
| 革命与拿破仑 / Revolution & Napoleon | 1789–1815         |
| 均势与技术萌芽 / Balance & Tech Dawn | 1815–1914         |



### 数据字段 / Data Fields

每场战争至少包含以下字段 / Each war contains at least:

```json
{
  "id": "hussite_wars",
  "name_zh": "胡斯战争",
  "name_en": "Hussite Wars",
  "start_year": 1419,
  "end_year": 1434,
  "region_zh": "波西米亚（今捷克）",
  "region_en": "Bohemia (modern Czechia)",
  "coordinates": [49.5, 15.0],
  "result_zh": "胡斯派分裂，圣杯派与皇帝联合获胜",
  "result_en": "Hussites splintered, Utraquists allied with Emperor",
  "key_battles": [...]   // 子战役列表 / sub-battle list
}
```



## 🛠️ 技术栈 / Tech Stack



## 📁 项目结构 / Project Structure



## 🚀 开发路线图 / Roadmap

### Phase 1: 数据整理 / Data Collection (预计 2-3 周)

- 收集胡斯战争到一战前的主要战争清单 (~50-80 场)
- 为每场战争标注坐标、时间、结果
- 为重要战争整理子战役数据 (~10-15 场重点战争)
- 输出标准化 JSON/CSV

### Phase 2: MVP 原型 / MVP Prototype (预计 2 周)

- 搭建 Flask 后端 API
- 实现基础地图 (Leaflet) + 战争标记点
- 实现时间轴滑块 (按年份筛选)
- 实现点击标记 → 右侧弹出概览卡片

### Phase 3: 交互增强 / Interaction Enhancement (预计 3 周)

- 实现地图缩放至战场区域动画
- 添加子战役标记点
- 实现战役卡片 (图片+文字)
- 添加战争对比功能

### Phase 4: 优化与发布 / Polish & Launch (预计 2 周)

- 中英文双语切换
- 移动端适配
- 性能优化 (数据懒加载)
- 部署上线



## 📊 数据来源 / Data Sources



## 🤝 贡献指南 / Contributing

**中文**
欢迎贡献！你可以通过以下方式参与：

- 补充或修正战争/战役数据
- 优化地图交互或UI设计
- 撰写新的战争详情介绍
- 提出功能建议或报告问题

请先阅读 [CONTRIBUTING.md](https://contributing.md/) 了解具体规范。

**English**
*Contributions are welcome! You can help by:*

- *Adding or correcting war/battle data*
- *Improving map interaction or UI design*
- *Writing detailed war introductions*
- *Suggesting features or reporting issues*

*Please read [CONTRIBUTING.md](https://contributing.md/) for guidelines.*



## 📝 示例数据预览 / Sample Data Preview

### 胡斯战争 / Hussite Wars

```json
{
  "id": "hussite_wars",
  "name_zh": "胡斯战争",
  "name_en": "Hussite Wars",
  "start_year": 1419,
  "end_year": 1434,
  "coordinates": [49.5, 15.0],
  "result_zh": "胡斯派分裂，圣杯派与皇帝西吉斯蒙德联合获胜",
  "result_en": "Hussites splintered, Utraquists allied with Emperor Sigismund",
  "key_battles": [
    {
      "name": "维特科夫山战役",
      "name_en": "Battle of Vítkov Hill",
      "year": 1420,
      "coordinates": [50.0833, 14.4167],
      "summary_zh": "扬·杰式卡率胡斯军以战车堡战术大胜第一次十字军，保卫布拉格。",
      "summary_en": "Jan Žižka's Hussites used wagon fort tactics to defeat the First Crusade, saving Prague."
    }
  ]
}
```



## 📄 许可证 / License

本项目采用 MIT 许可证。详见 LICENSE 文件。

This project is licensed under the MIT License - see the LICENSE file for details.



## 📧 联系方式 / Contact

- 项目维护者 / Maintainer: Ralph957
- GitHub: [Ralph957 (github.com)](https://github.com/Ralph957)
- 邮箱 / Email: 1449860166@qq.com



**⭐ 如果这个项目对你有帮助，欢迎给它一个 Star！**
*⭐ If this project is helpful to you, please give it a Star!*