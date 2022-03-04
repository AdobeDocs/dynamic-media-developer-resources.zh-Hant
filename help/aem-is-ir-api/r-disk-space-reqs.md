---
description: '除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求 '
solution: Experience Manager
title: 磁碟空間要求和建議
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# 磁碟空間要求和建議{#disk-space-requirements-and-recommendations}

除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>說明/預設位置/設定</b> </th> 
   <th class="entry"> <b>計算/建議</b> </th> 
   <th class="entry"> <b>備註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>源影像、字型、ICC配置檔案</b> </p> <p> <span class="filepath"> <span class="varname"> 安裝資料夾 </span>/影像 </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>不同；請參閱下面的注釋。 </p> </td> 
   <td> <p>只需映像伺服器可訪問；伺服器從不修改資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP響應資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> 安裝資料夾 </span>/cache/is響應 </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2;建議至少2 GB。 </p> </td> 
   <td> <p>此快取還儲存嵌套/嵌入資料和外來源影像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>影像目錄資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> 安裝資料夾 </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>允許目錄資料夾使用1.5倍的空間。 </p> </td> 
   <td> <p>在初始載入目錄時填充。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>日誌資料</b> </p> <p> <span class="filepath"> <span class="varname"> 安裝資料夾 </span>/日誌 </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS:：日誌檔案 </span> </p> <p> <span class="codeph"> SV:：日誌檔案 </span> </p> </td> 
   <td> <p>100 MB或更高。 </p> </td> 
   <td> <p>視日誌配置和伺服器使用情況而定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>映像伺服器臨時檔案</b> </p> <p> <span class="filepath"> <span class="varname"> 安裝資料夾 </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MB的容量足以滿足大多數使用。 </p> </td> 
   <td> <p>短期資料；對於PTIFF和某些響應影像格式以外的源影像可能需要。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 源映像的磁碟空間要求 {#section-317da75099ad480d9a461c7e706d4f1c}

建議使用影像轉換器命令行工具(IC)將所有源影像轉換為金字塔TIFF檔案格式(PTIFF)。 此轉換可確保所有應用程式的映像服務的最佳運行時效能。 雖然映像伺服器可以處理IC接受的所有源檔案格式，但Dynamic Media不支援這種用途。

使用PTIFF檔案時，以下經驗規則可幫助您確定空間要求。

*`total_space`* （位元組）= *`number_of_images`* x(2000 +) *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* 所有原始源影像的平均像素大小（寬度x高度）。 例如，如果原始影像通常在2k x 2k像素左右，則這將是4M像素。
* *`avg_num_components`* 取決於影像類型。 對於大多數RGB影像，它為3，對於大多數CMYK或RGBA影像，它為4。 如果半部影像為RGB，另一半為RGBA，則使用3.5。
* *`p_factor`* 取決於使用IC轉換影像時的壓縮類型和質量設定。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF壓縮</b> </th> 
   <th class="entry"> <b><i>p因子</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>未壓縮 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>壓縮 </p> </td> 
   <td> <p> 25-0.75，視圖而定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG壓縮 </p> </td> 
   <td> <p> 1(典型JPEG質量95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似不考慮檔案系統開銷。 磁碟上的實際空間可以大得多。

**範例**

映像服務部署預期使用30,000個低解析度舊映像，平均大小為500x500RGB像素。 新的打印質量影像資料預計將以每年10 000的速率添加。 典型CMYK影像大小為4k x 6k位元組。 所有資料都以高質量JPEG壓縮。 3年使用後的磁碟空間總量估計如下：

*`total_space`* = 30,000 x(2k + 0.5k x 0.5k x 3 x 0.1)+ 3 x 10,000 x(2k + 4k x 6k x 4 x 0.1)= 2.2 G + 268 GB =大約270 GB

為保證最佳質量，可採用壓縮(zip)壓縮。 假設 *`p_factor`* 0.4，所需磁碟空間總量大約4倍。 在這種情況下，略高於1 TB。
