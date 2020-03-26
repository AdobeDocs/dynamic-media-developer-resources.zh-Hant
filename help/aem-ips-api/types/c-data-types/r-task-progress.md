---
description: 任務進度資訊。
seo-description: 任務進度資訊。
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TaskProgress{#taskprogress}

任務進度資訊。

語法

## 參數 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> taskType <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 任務類型說明。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 已 <span class="varname"> 處理數</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 已處理的任務項數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 處 <span class="varname"> 理數</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 當前正在處理的任務項數。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 待 <span class="varname"> 定數</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 待定任務項目數（尚未處理）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 進 <span class="varname"> 度</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> %進度（範圍0.0 - 1.0）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 進 <span class="varname"> 度訊息</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 進度訊息。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上 <span class="varname"> 次進度更新</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次更新進度資訊的時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> taskItemProgressArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：TaskItemProgressArray</span> </td> 
   <td colname="col3"> 任務項的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 任 <span class="varname"> 務狀態</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">值包括： 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> 未知</span>:當任務監視器在狀態之間轉換時。 </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> 新增</span>:任務監視器已建立，但尚未接受任務。 </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> 處理</span>:任務監視程式正在主動處理任務。 </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> 停止</span>:任務監視程式正在停止作業，因為有停止作業請求。 </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> 完成</span>:已完成分配給任務監視程式作業的作業。 </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> 失敗</span>:表示嚴重錯誤。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

