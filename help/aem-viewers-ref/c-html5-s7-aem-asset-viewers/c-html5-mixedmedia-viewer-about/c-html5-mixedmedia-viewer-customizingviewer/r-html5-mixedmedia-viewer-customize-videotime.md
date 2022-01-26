---
title: 視頻時間
description: 視頻時間是顯示當前播放視頻的當前時間和持續時間的數字顯示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 視頻時間{#video-time}

視頻時間是顯示當前播放視頻的當前時間和持續時間的數字顯示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

視頻時間字型系列、字型大小和字型顏色是CSS可以控制的屬性之一。 也可以通過CSS相對於包含該控制項的控制欄來定位。

視頻時間的外觀由以下CSS類選擇器控制：

```
.s7mixedmediaviewer .s7videotime
```

## 視頻時間的CSS屬性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂部 </span> </p> </td> 
   <td colname="col2"> <p>從上邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右側 </span> </p> </td> 
   <td colname="col2"> <p>從右邊框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 視頻時間控制的寬度。 此屬性是Internet Explorer 8或更高版本才能正常運行的必需屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型系列 </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字型大小 </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用於時間顯示文本的字型顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 範例 {#section-e8caea0a303c425a8a637c2a47c06355}

將視頻時間設定為淺灰色（十六進位） `#BBBBBB`)，大小為12像素，距控制欄頂部15像素，距控制欄右邊緣80像素。

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
