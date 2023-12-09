---
title: Shedding light on viable decarbonization paths--Project VisCEADs
date: 2023-12-06T07:42:52.984Z
draft: false
featured: true
authors:
  - Han-Teng Liao
  - Chung-Lien Pan
tags:
  - "#CarbonEmissionManagement"
  - GreenDigitalTransformation
  - TechnologyRoadmapping
  - BusinessModel
  - SmartDigitalPlatform
categories:
  - Precision Decarbonization
  - Social Network Analysis
  - Input-Output Analysis
---
<style>
h1{font-size: 2.75rem; important!}
h2{font-size: 2rem; important!}
.article-container {max-width:100vw; !important}
.info-vis {
    width: 100vw;
    height: 100vh;
}</style>
Decarbonization requires voluntary will and participation, and values provide incentives. 

Only by providing true values to individuals and organizations, the climate goal of GHG emission reduction can be achieved.  It requires the incorporation of GHG and carbon emission information into the production, distribution, consumption and investment processes of human activities.  

The **dual-carbon management and service platforms**，or simply smart digital platforms of carbon and GHG emission data platforms, aims to introduce such information into the operations and management of enterprises and government organizations at various levels.  They embodies the main task of the "twin transition" or green digital transformation of human activities and interactions with the planet.  

How might we define, design and develop such a platform？

<div class="p-3 mb-2 bg-light text-dark" markdown="1">

This project (visCEADs, or visualization of the Carbon Emission Accounts and Datasets) utilizes the following resources released by various organizations.  They provide vital information and best practices for industries and government bodies to achieve "precision decarbonization," by which Oxford Roadmapping means the viable and actionable actions for GHG reduction based on science-based data：

* China's [　“Dual-Carbon Management Digital Platform”　Industry Standard](https://www.isc.org.cn//profile//2023/06/13/60cbc996-47cc-45be-bf0d-06053fbe57de.pdf) 
* China-led international collaboration research network [Carbon Emission Accounts and Datasets (CEADs)](https://www.ceads.net.cn/)
* The International Telecommunication Union (ITU), the United Nations specialized agency for information and communication technologies (ICTs) recommendations on green digital transformation standards:  [L.1470](https://www.itu.int/rec/T-REC-L.1470-202001-I/en) [L.1480](https://www.itu.int/rec/T-REC-L.1480-202212-I)
* Oxford Roadmapping's [ platform business model design for smart digital platforms of carbon neutral management and services ](https://oxon8.netlify.app/post/2023-02-20-smart-digital-platforms-carbon-neutral-management-services/)(developed based on the above standard and data resources)

</div>

<!--more-->

<div class=".h1 fs-1 bg-success text-center" markdown="1">

# <i class="ai ai-figshare ai-1x fa-spin"></i>visCEADs: Visualizing the Carbon Emission Accounts and Datasets (CEADs) for Emission Insights into Industrial Inputs and Outputs

</div>

Developed by Oxford Roadmapping (Oxon8), the visCEADs project has systematically incorporates the core Chinese dataset of the [Carbon Emission Accounts and Datasets (CEADs)](https://www.ceads.net.cn/).  For building viable prototypes, the visCEADs project has applied data science for data cleaning and transformation, followed human-centered computing design of network visualization, and considered the standard requirements of China's [“Dual-Carbon Management Digital Platform”](https://www.isc.org.cn//profile//2023/06/13/60cbc996-47cc-45be-bf0d-06053fbe57de.pdf) and [platform business models](https://oxon8.netlify.app/post/2023-02-20-smart-digital-platforms-carbon-neutral-management-services/).

This prototype demonstrates one viable systematic approach in incorporating carbon emission and industrial input-output data at various junctures of operations and management across all industrial sectors, ranging from production to consumption.  It embodies the potential of integration of system engineering and system innovations. With the purpose to encourage scientific and value-added emission reduction efforts, such innovations highlight the science-based on one hand, and the value-added (and thus market-relevant) approach on the other, integrated approach to combine carbon emission and industrial input-output data.  This integrated approach benefits individuals and industries with reasonable carbon emission accounting and reduction regimes that reward values to emission reduction based on data. 

Since the founding of the company in early 2023, Oxford Roadmapping has produced the first Prototype A for the visCEADs during July to December of 2023. 

<div class=".h2 fs-2 bg-success text-center" markdown="1">

## Showcase of Prototype A<i class="ai ai-pubpeer ai-2x fa-shake"></i>

</div>

The prototype of the visCEADs project showcases one way to extract insights from both the CO2 emission inventory and the input-output table data of 42 industrial sectors and 31 provinces and cities in China.  Conceptually, it combines social network analysis and the 3B framework (backbone, baselines, and benchmarks) to build the core visualization module for  [“dual-carbon management digital platforms”](https://www.isc.org.cn//profile//2023/06/13/60cbc996-47cc-45be-bf0d-06053fbe57de.pdf) or other similar smart digital platforms using similar datasets.

As shown below, the visualization outcomes are interactive! You can also [click on this for full-screen experieince](./visualization.zh.html).
 
<iframe class = "info-vis" src="./visualization.en.html" width="100%" style="border:none;"></iframe>

### 项目迸度

* 2023/04：项目启动前[《碳中和管理服务数智平台》](https://oxon8.netlify.app/post/2023-02-20-smart-digital-platforms-carbon-neutral-management-services/)获录稿发表，探究平台商业模式与数智平台的机理

* 2023/05：项目启动-- 科研与市研确立数据及潜在需求 （如[企业碳盘查SaaS服务](https://www.skyco2.com/ncem/index.html)、[温室气体排放核算标准库](https://www.skyco2.com/)）等等。

* 2023/07：项目需求-- 确立数据来源及潜在需求，对标中国互联网协会发布的“双碳管服数字平台”标准（正式名称《碳达峰碳中和管理与服务平台第1部分：架构规范》）与国际前沿专利及科研，设计中国碳核算数据库可视化技术路线，确立3B框架 (backbone, baseline, and benchmark, ) 来转化数据科学及机器学习技术成为产业脱碳情报的骨架 (backbone)、基线 (baseline)、与标杆 (benchamrk)：

    * 骨架 (backbone):

基本历史与当下的产业投入产出结构，降低产业与地方脱碳转型脱离现实、转错方向、抓错重点等重大策略风险。

    * 基线 (baseline):

以地方各省及全中国的碳排数据、进阶碳排强度计量、及产业整体与平均数据作为基线(baseline)，产出并提供产业与地方历史及现实数据作为‘精准脱碳’旅程的基础指标，作为下一步设计一般性KPI、及客制化KPI的基础，以形成按产业及地域特性“量身定制”的碳达峰碳中和管理与服务平台

* 2023/12：交付原型成果A--含可交互功能之全套分省/地域之产业结构图
