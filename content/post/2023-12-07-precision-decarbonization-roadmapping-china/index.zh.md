---
title:  '中国各省精准脱碳图谱@COP28'
date: 2023-12-07
categories:
- Precision Decarbonization
- 精准脱碳
- Decarbonization Roadmapping
- 脱碳路线图
tags:
- COP28
- 联合国气候大会
- Carbon management
- 碳排管理
- Green Digital Transformation
- 双化协同
- 数字化绿色化双转型
---

    <script src="https://jsd.cdn.zzko.cn/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js" integrity="sha256-YMa+wAM6QkVyz999odX7lPRxkoYAan8suedu4k2Zur8=" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://jsd.cdn.zzko.cn/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" integrity="sha256-MBffSnbbXwHCuZtgPYiwMQbfE7z+GOZ7fBPCNB06Z98=" crossorigin="anonymous">
<!-- Custom Stylesheet -->
<style>
html {
  font-size: 12px;
  height: 100vh;
}
.row {
  height: 100vh;
}
</style>


<!-- Custom javascript for loading Frame -->
<script>
    function updateDiv(inputID, formattedStringFilename)
    { 
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

    <!-- Custom styles for this template -->
  </head>
  <body>
  
  <div class="container">
  <div class="row" >
    <div class="col-sm-2"  height="100%" style="background-color:lightgray;">
      <!-- Region Input -->
        <label for="RegionInput" class="form-label fs-3">Input Region</label>
      <input  value="" class="form-control" list="RegionOptions" id="RegionInput" placeholder="Choose a region...">
      <datalist id="RegionOptions">
        <option data-id="BJ" name="北京 BJ" value="北京 BJ">
        <option data-id="TJ" name="天津 TJ" value="天津 TJ">
        <option data-id="HE" name="河北 HE" value="河北 HE">
        <option data-id="SX" name="山西 SX" value="山西 SX">
        <option data-id="NM" name="内蒙古 NM" value="内蒙古 NM">
        <option data-id="LN" name="辽宁 LN" value="辽宁 LN">
        <option data-id="JL" name="吉林 JL" value="吉林 JL">
        <option data-id="HL" name="黑龙江 HL" value="黑龙江 HL">
        <option data-id="SH" name="上海 SH" value="上海 SH">
        <option data-id="JS" name="江苏 JS" value="江苏 JS">
        <option data-id="ZJ" name="浙江 ZJ" value="浙江 ZJ">
        <option data-id="AH" name="安徽 AH" value="安徽 AH">
        <option data-id="FJ" name="福建 FJ" value="福建 FJ">
        <option data-id="JX" name="江西 JX" value="江西 JX">
        <option data-id="SD" name="山东 SD" value="山东 SD">
        <option data-id="HA" name="河南 HA" value="河南 HA">
        <option data-id="HB" name="湖北 HB" value="湖北 HB">
        <option data-id="HN" name="湖南 HN" value="湖南 HN">
        <option data-id="GD" name="广东 GD" value="广东 GD">
        <option data-id="GX" name="广西 GX" value="广西 GX">
        <option data-id="HI" name="海南 HI" value="海南 HI">
        <option data-id="CQ" name="重庆 CQ" value="重庆 CQ">
        <option data-id="SC" name="四川 SC" value="四川 SC">
        <option data-id="GZ" name="贵州 GZ" value="贵州 GZ">
        <option data-id="YN" name="云南 YN" value="云南 YN">
        <option data-id="XZ" name="西藏 XZ" value="西藏 XZ">
        <option data-id="SN" name="陕西 SN" value="陕西 SN">
        <option data-id="GS" name="甘肃 GS" value="甘肃 GS">
        <option data-id="QH" name="青海 QH" value="青海 QH">
        <option data-id="NX" name="宁夏 NX" value="宁夏 NX">
        <option data-id="XJ" name="新疆 XJ" value="新疆 XJ">      </datalist>
      
      <!-- Year Input -->
        <label for="YearInput" class="form-label fs-3">Input Year</label>
      <input value="201" class="form-control" list="YearOptions" id="YearInput" placeholder="Type to search...">
      <datalist id="YearOptions">
        <!--<option value="2017new">-->
        <option value="2017">
        <option value="2015">
        <option value="2012">
      </datalist>
      <button onclick="loadIframe()" type="button" class="btn btn-outline-primary">读取可视化页面</button>
      <br/>
      <h8>选定地域及时间，读取产业投入产出关系结构，及其碳排强度及量。</h8>
      <div id='Filename'  class="alert alert-dark text-end fs-6"></div>
      <figcaption class="alert alert-info">
          <cite>廖汉腾. (2023). 中国各省精准脱碳图谱：高碳排主要产业及其关系网. Oxford Roadmapping 澳恪森数智科技服务(广州)有限公司. <br/>注：此图将发表，在发表前请勿正式引用。</cite>
      </figcaption>
    </div>
    <div class="col-sm-10"  height="100%" >
            <!-- Iframe Content -->
            <iframe id="iframeContent" height="100%" width="100%" style="border:none;"></iframe>

    </div>
  </div>
</div>
  