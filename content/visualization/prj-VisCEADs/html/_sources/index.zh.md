# VisCEADs：投入产出网络

此说明文档解释如何使用、诠释、应用 VisCEADs **[投入产出网络仪表盘](https://oxon8.netlify.app/visualization/prj-visCEADs/index.zh)** ，为中国各省各行业脱碳路线提供科学实证基础。

包括但不限于对**部门脱碳方法/行业脱碳法 (SDA)** 及 **净零经济(Net Zero Economy)** 启示。此可视化目前基于 [中国碳核算数据库](https://www.ceads.net.cn/)(Carbon Emission Accounts & Datasets，CEADs)  数据。

核心应用问题为：各省各行业要如何**发展与污染**有效脱钩（包括关键指标**碳排强度**），打断经济发展与环境污染水平之间的关系。

本说明文档的大纲如下：

```{tableofcontents}
```

# 目标读者
## 一般用户（包括政策制定者、产业经营者、研究者）

使用VisCEADs投入产出网络仪表盘可以探究以下应用问题：
* 要如何具体应用**科学证据及方法**，建构**碳中和的时间表、路线图、施工图**。
	* 参考：2021年4月30日习近平总书记在中共中央政治局第二十九次集体学习时强调，“**各级党委和政府**要拿出实现碳达峰、碳中和的时间表、路线图、施工图”
* 针对一省/地区：
	* [ ] 要减多少？减哪里？减多快？
	* 此省/地的主要产业投入产出特性为何？
		* [v] 关键指标（如**CO2排放**、**碳排强度**、投入、产出、等）**前列部门行业**有哪些？
		* [v] 关键指标历年走向对脱碳路线的意涵？
		* [v] **前列部门行业**的投入产出**桑基图**对**供应链网络**绿色化的意涵？
* 针对一行业：
	* [ ] 要减多少？减哪里？减多快？
	* [ ] 在中国各省的关键指标表现最佳及最差的分布为何？
	* [ ] 针对各省的比较优势，如何**发展与污染**有效脱钩的区域布局或区域政策？

## 智能碳排管理平台开发者

使用VisCEADs投入产出网络仪表盘可以共同开发以下应用发展可能：
* 要如何使用生成**数据与文本合成数据**，开发人工智能问答系统，回答用户如以下问题：**广东在2060年达成碳中和时间表及产业投入产出路线图應应为何？**
	* 技术路线：使用 [Panel Chat](https://github.com/holoviz-topics/panel-chat-examples)案例，建构并应用 [LangChain](https://python.langchain.com/docs/get_started/introduction), [OpenAI](https://openai.com/blog/chatgpt), [Mistral](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwjZtP35yvSBAxU00wIHHerUDZAQFnoECBEQAQ&url=https%3A%2F%2Fdocs.mistral.ai%2F&usg=AOvVaw2qpx09O_zOzSksgjBKiJY_&opi=89978449), [Llama](https://ai.meta.com/llama/), 等语言模型。
* 要如何使用生成**智能数据科学及可视化工具**，开发脱碳专用人工智能可视化系统，回答开发用户如以下问题：**请生成中国碳核算数据库产业投入产出路数据可视化代码，用来探索公共管理部门的脱碳走势？**
	* 技术路线：使用[PandasAI](https://docs.pandas-ai.com/intro)