---
title:  '中国各省精准脱碳图谱：高碳排主要产业及其关系网：@COP28'
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

<html lang="en" data-bs-theme="auto">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="Interacting with CEADs visualization outcomes  using Dropdowns · Bootstrap v5.3">
    <meta name="author" content="Liao, Han-Teng, Oxford Roadmapping">
    <title></title>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.min.js" integrity="sha256-YMa+wAM6QkVyz999odX7lPRxkoYAan8suedu4k2Zur8=" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" integrity="sha256-MBffSnbbXwHCuZtgPYiwMQbfE7z+GOZ7fBPCNB06Z98=" crossorigin="anonymous">
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
  var locale = 'en';
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
        <option data-id="AH" name="Anhui AH" value="Anhui AH">
        <option data-id="BJ" name="Beijing BJ" value="Beijing BJ">
        <option data-id="CQ" name="Chongqing CQ" value="Chongqing CQ">
        <option data-id="FJ" name="Fujian FJ" value="Fujian FJ">
        <option data-id="GD" name="Guangdong GD" value="Guangdong GD">
        <option data-id="GS" name="Gansu GS" value="Gansu GS">
        <option data-id="GX" name="Guangxi GX" value="Guangxi GX">
        <option data-id="GZ" name="Guizhou GZ" value="Guizhou GZ">
        <option data-id="HA" name="Henan HA" value="Henan HA">
        <option data-id="HB" name="Hubei HB" value="Hubei HB">
        <option data-id="HE" name="Hebei HE" value="Hebei HE">
        <option data-id="HI" name="Hainan HI" value="Hainan HI">
        <option data-id="HL" name="Heilongjiang HL" value="Heilongjiang HL">
        <option data-id="HN" name="Hunan HN" value="Hunan HN">
        <option data-id="JL" name="Jilin JL" value="Jilin JL">
        <option data-id="JS" name="Jiangsu JS" value="Jiangsu JS">
        <option data-id="JX" name="Jiangxi JX" value="Jiangxi JX">
        <option data-id="LN" name="Liaoning LN" value="Liaoning LN">
        <option data-id="NM" name="Inner Mongolia NM" value="Inner Mongolia NM">
        <option data-id="NX" name="Ningxia NX" value="Ningxia NX">
        <option data-id="QH" name="Qinghai QH" value="Qinghai QH">
        <option data-id="SC" name="Sichuan SC" value="Sichuan SC">
        <option data-id="SD" name="Shandong SD" value="Shandong SD">
        <option data-id="SH" name="Shanghai SH" value="Shanghai SH">
        <option data-id="SN" name="Shaanxi SN" value="Shaanxi SN">
        <option data-id="SX" name="Shanxi SX" value="Shanxi SX">
        <option data-id="TJ" name="Tianjin TJ" value="Tianjin TJ">
        <option data-id="XJ" name="Xinjiang XJ" value="Xinjiang XJ">
        <option data-id="XZ" name="Tibet XZ" value="Tibet XZ">
        <option data-id="YN" name="Yunnan YN" value="Yunnan YN">
        <option data-id="ZJ" name="Zhejiang ZJ" value="Zhejiang ZJ">
      </datalist>
      
      <!-- Year Input -->
        <label for="YearInput" class="form-label fs-3">Input Year</label>
      <input value="201" class="form-control" list="YearOptions" id="YearInput" placeholder="Type to search...">
      <datalist id="YearOptions">
        <!--<option value="2017new">-->
        <option value="2017">
        <option value="2015">
        <option value="2012">
      </datalist>
      <button onclick="loadIframe()" type="button" class="btn btn-outline-primary">Load Page</button><br/>
      <h8>Visualization of industrial structure and its carbon emission amount and intensity</h8>
      <div id='Filename'  class="alert alert-dark text-end fs-6"></div>
      <figcaption class="alert alert-info">
          <cite>Liao, Han-Teng. (2023). Precision Decarbonization Roadmap for Chinese Provinces: Exploring the industrial input-output relations along with carbon emission (and intensity) data from CEADs. Oxford Roadmapping . <br/>Note: Please kindly cite this pa</cite>
      </figcaption>

    </div>
    <div class="col-sm-10"  height="100%" >
            <!-- Iframe Content -->
            <iframe id="iframeContent" height="100%" width="100%" style="border:none;"></iframe>

    </div>
  </div>
</div>
  
  
  </body>
  

</html>