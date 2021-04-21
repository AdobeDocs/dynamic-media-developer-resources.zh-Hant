---
description: '除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求 '
solution: Experience Manager
title: 磁碟空間要求和建議
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# 磁碟空間要求和建議{#disk-space-requirements-and-recommendations}

除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>說明／預設位置／設定為</b> </th> 
   <th class="entry"> <b>計算／建議</b> </th> 
   <th class="entry"> <b>備註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>來源影像、字型、ICC描述檔</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>不同；請參閱以下注釋。 </p> </td> 
   <td> <p>只需影像伺服器可存取；伺服器不會修改資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP回應資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;建議至少2 GB。 </p> </td> 
   <td> <p>此快取也儲存巢狀／內嵌資料和外來來源影像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>影像目錄資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>允許目錄資料夾使用1.5倍的空間。 </p> </td> 
   <td> <p>在初次載入目錄時填入。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>日誌資料</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 MB以上。 </p> </td> 
   <td> <p>視記錄設定和伺服器使用而定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>映像伺服器臨時檔案</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MB的容量足以滿足大多數用途。 </p> </td> 
   <td> <p>短期資料；可能需要PTIFF以外的來源影像和某些回應影像格式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 源映像{#section-317da75099ad480d9a461c7e706d4f1c}的磁碟空間要求

建議使用「影像轉換器」命令列工具(IC)，將所有來源影像轉換為金字塔TIFF檔案格式(PTIFF)。 此轉換可確保所有應用程式的影像伺服最佳執行時期效能。 雖然影像伺服器可處理IC所接受的所有原始檔案格式，但Dynamic Media不提供此類用途的支援。

使用PTIFF檔案時，下列經驗法則可協助您判斷空間需求。

*`total_space`* （位元組）=  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* 所有原始來源影像的平均像素大小（寬x高）。例如，如果原始影像通常在2k x 2k像素左右，則此為4M像素。
* *`avg_num_components`* 視影像類型而定。對於大部分的RGB影像，它是3，對於大部分的CMYK或RGBA影像，它是4。 如果一半的影像是RGB，另一半是RGBA，請使用3.5。
* *`p_factor`* 視使用IC轉換影像時的壓縮類型和品質設定而定。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF壓縮</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>未壓縮 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75，視影像而定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG壓縮 </p> </td> 
   <td> <p> 1（JPEG品質的典型值95） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似不考慮檔案系統開銷。 磁碟上的實際空間可以大得多。

**範例**

「影像伺服」部署預計會使用30,000張低解析度的舊版影像，平均大小為500x500 RGB像素。 新的列印品質影像資料預計每年可新增10,000張。 典型的CMYK影像大小為4k x 6k位元組。 所有資料都將以高品質進行JPEG壓縮。 3年使用後的磁碟空間總量估計如下：

*`total_space`* = 30,000 x(2k + 0.5k x 0.5k x 3 x 0.1)+ 3 x 10,000 x(2k + 4k x 6k x 4 x 0.1)= 2.2 G + 268 GB =大約270 GB

為獲得最佳品質，可使用Deflate(zip)壓縮。 假設&#x200B;*`p_factor`*&#x200B;為0.4，則所需磁碟空間總量大約是4倍。 在這種情況下，略高於1 TB。
