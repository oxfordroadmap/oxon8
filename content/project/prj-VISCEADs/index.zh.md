---
title: 照亮产业「精准脱碳」之路--2023VISCEADs
subtitle: 中国碳核算数据库可视化项目--碳中和数智平台、双碳管服数字平台的骨架、基线、与标杆
date: 2023-12-07T07:42:52.984Z
summary: 碳核算数据系统创新，定义、设计并制作碳中和数智平台、双碳管服数字平台的骨架、基线、与标杆
draft: false
featured: true
authors: 
  - Han-Teng Liao
  - Chung-Lien Pan
tags:
  - 【2023VISCEADs】
  - Carbon management
  - Green Digital Transformation
  - Smart digital platforms
  - Technological roadmapping
  - Business models
categories:
  - Agro-food
image:
  filename: https://upload.wikimedia.org/wikipedia/commons/thumb/b/be/Vertical_Tower_Aquaponic_System.jpg/617px-Vertical_Tower_Aquaponic_System.jpg
  focal_point: Smart
  preview_only: false
---
### 项目迸度

* 2023/04：项目启动前[《碳中和管理服务数智平台》](https://oxon8.netlify.app/post/2023-02-20-smart-digital-platforms-carbon-neutral-management-services/)获录稿发表，探究平台商业模式与数智平台的机理

* 2023/05：项目启动-- 科研与市研确立数据及潜在需求 （如[企业碳盘查SaaS服务](https://www.skyco2.com/ncem/index.html)、[温室气体排放核算标准库](https://www.skyco2.com/)）等等。

* 2023/07：项目需求-- 确立数据来源及潜在需求，对标中国互联网协会发布的“双碳管服数字平台”标准（正式名称《碳达峰碳中和管理与服务平台第1部分：架构规范》）与国际前沿专利及科研，设计中国碳核算数据库可视化技术路线，确立3B框架 (backbone, baseline, and benchmark, ) 来转化数据科学及机器学习技术成为产业脱碳情报的骨架 (backbone)、基线 (baseline)、与标杆 (benchamrk)：

    * 骨架 (backbone):
      * 基本历史与当下的产业投入产出结构，降低产业与地方脱碳转型脱离现实、转错方向、抓错重点等重大策略风险。

    * 基线 (baseline):
      * 以地方各省及全中国的碳排数据、进阶碳排强度计量、及产业整体与平均数据作为基线(baseline)，作为‘精准脱碳’旅程的基础指标。这些基于产业与地方历史及现实数据作为下一步设计一般性KPI、及客制化KPI的基础，以形成按产业及地域特性“量身定制”的碳达峰碳中和管理与服务平台。

    * 标杆 (benchamrk):
      * 以基线为基础（可跨省或跨行业比较）及比对历史改变，<mark>订立科学基础减量目标倡议(SBTi)的标杆计量及演算法</mark>，以数据驱动决策，产出一批<mark>最佳实践标杆</mark>、<mark>行业标兵</mark>企业、<mark>地方标兵</mark>单位等等。

* 2023/12：交付原型成果A--含可交互功能之全套分省/地域之产业结构图


### 项目原型成果A展示


<style>
.info-vis {
    width: 100vw;
    height: 100vh;
}</style>


<div class="info-vis alert alert-success d-flex align-items-center" role="alert">
	<div class="text-success">此图有🪄交互功能（试试拖拉、多手指平移、缩放页面及🖱️鼠标悬停效果）</div>
	<!-- Info-vis Main Part-->
	<div class="row align-items-center" >
	<div class="col-10"  height="100vh" >
		<!-- Iframe Content -->
		<iframe id="iframeContent" height="100%" width="100%" style="border:none;"></iframe>
	</div>
		<div class="col-2 order-first"  height="100vh" style="background-color:lightgray;">
			<!-- Region Input -->
			<label for="RegionInput" class="form-label fs-3">地域</label>
			<input  value="" class="form-control" list="RegionOptions" id="RegionInput" placeholder="输选地方...">
			<datalist id="RegionOptions"><option data-id="BJ" name="北京 BJ" value="北京 BJ"><option data-id="TJ" name="天津 TJ" value="天津 TJ"><option data-id="HE" name="河北 HE" value="河北 HE"><option data-id="SX" name="山西 SX" value="山西 SX"><option data-id="NM" name="内蒙古 NM" value="内蒙古 NM"><option data-id="LN" name="辽宁 LN" value="辽宁 LN"><option data-id="JL" name="吉林 JL" value="吉林 JL"><option data-id="HL" name="黑龙江 HL" value="黑龙江 HL"><option data-id="SH" name="上海 SH" value="上海 SH"><option data-id="JS" name="江苏 JS" value="江苏 JS"><option data-id="ZJ" name="浙江 ZJ" value="浙江 ZJ"><option data-id="AH" name="安徽 AH" value="安徽 AH"><option data-id="FJ" name="福建 FJ" value="福建 FJ"><option data-id="JX" name="江西 JX" value="江西 JX"><option data-id="SD" name="山东 SD" value="山东 SD"><option data-id="HA" name="河南 HA" value="河南 HA"><option data-id="HB" name="湖北 HB" value="湖北 HB"><option data-id="HN" name="湖南 HN" value="湖南 HN"><option data-id="GD" name="广东 GD" value="广东 GD"><option data-id="GX" name="广西 GX" value="广西 GX"><option data-id="HI" name="海南 HI" value="海南 HI"><option data-id="CQ" name="重庆 CQ" value="重庆 CQ"><option data-id="SC" name="四川 SC" value="四川 SC"><option data-id="GZ" name="贵州 GZ" value="贵州 GZ"><option data-id="YN" name="云南 YN" value="云南 YN"><option data-id="XZ" name="西藏 XZ" value="西藏 XZ"><option data-id="SN" name="陕西 SN" value="陕西 SN"><option data-id="GS" name="甘肃 GS" value="甘肃 GS"><option data-id="QH" name="青海 QH" value="青海 QH"><option data-id="NX" name="宁夏 NX" value="宁夏 NX"><option data-id="XJ" name="新疆 XJ" value="新疆 XJ"></datalist>
			<!-- Year Input -->
			<label for="YearInput" class="form-label fs-3">时间</label>
			<input value="201" class="form-control" list="YearOptions" id="YearInput" placeholder="输选年度">
			<datalist id="YearOptions"><option value="2017new"><option value="2017"><option value="2015">	<option value="2012"></datalist>
			<!-- Button-->
			<button onclick="loadIframe()" type="button" class="btn btn-outline-primary">读取可视化页面</button><br/>
			<h8>选定地域及时间，读取产业投入产出关系结构，及其碳排强度及量。</h8>
			<figcaption class="alert alert-info">
				<cite>廖汉腾. (2023). 中国各省精准脱碳图谱：高碳排主要产业及其关系网. Oxford Roadmapping 澳恪森数智科技服务(广州)有限公司. <br/>注：此图将发表，在发表前请勿正式引用。</cite>
			</figcaption>
			<!-- Filename-->
			<div id='Filename'  class="alert alert-dark text-end fs-6"></div>
		</div>
	</div>
</div>

<!-- Custom javascript for loading Frame -->
<script>
    function updateDiv(inputID, formattedStringFilename){ 
        document.getElementById(inputID).innerHTML = formattedStringFilename ;
    } 
function loadIframe() {
  var inputReg = document.getElementById('RegionInput').value;  
  var listReg = document.getElementById('RegionOptions');
  var inputRegID = listReg.options.namedItem( inputReg ).getAttribute('data-id');  
  var inputYear = document.getElementById('YearInput').value;
  var iframe = document.getElementById('iframeContent');
  var indicator = '_R69_';
  var perc = 5;
  var locale = 'zh-hans';
  var formattedStringFilename = `./visualization/NetVis-${inputRegID}.${inputYear}-${indicator}.${perc}.${locale}.html`;
  updateDiv ('Filename', formattedStringFilename);
  iframe.src = formattedStringFilename;
}</script>




### 项目负责人
廖汉腾

---

### 关于澳恪森数智科技

澳恪森数智科技，简称Oxon8，全名为澳恪森数智科技服务（广州）有限公司，创新数智平台与绿色金融科技的设计，助组织与个人的双化协同发展及精准脱碳之旅。

![icon.webp](icon.webp)

澳恪森Oxon8为行业﹑智库﹑政府等提供基于专利分析﹑科学计量﹑知识图谱等等数据情报，合作开展集科技研发﹑科技服务﹑成果转化﹑系统集成﹑人才培养﹑等科技创新公共及商业服务，运用前瞻情报连结在地及全球网络。
