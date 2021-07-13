---
description: '除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求 '
solution: Experience Manager
title: 磁碟空間要求和建議
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# 磁碟空間要求和建議{#disk-space-requirements-and-recommendations}

除了安裝軟體所需的空間外，映像服務還有以下磁碟空間要求：

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>說明/預設位置/設定為</b> </th> 
   <th class="entry"> <b>計算/建議</b> </th> 
   <th class="entry"> <b>備註</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>源影像、字型、ICC配置檔案</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>不同；請參閱下方的評論。 </p> </td> 
   <td> <p>只需要映像伺服器可訪問；伺服器不會修改資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP回應資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;建議至少2 GB。 </p> </td> 
   <td> <p>此快取還儲存嵌套/嵌入的資料和外源映像。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>影像目錄資料快取</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>允許目錄資料夾使用1.5倍的空間。 </p> </td> 
   <td> <p>在初始載入目錄時填入。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>記錄資料</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100兆位元組或更多。 </p> </td> 
   <td> <p>視記錄設定和伺服器使用情況而定。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>映像伺服器臨時檔案</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MB的容量足以滿足大多數使用需要。 </p> </td> 
   <td> <p>短期資料；可能需要PTIFF和某些響應影像格式以外的源影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 源映像的磁碟空間要求 {#section-317da75099ad480d9a461c7e706d4f1c}

建議使用「影像轉換器」命令行工具(IC)將所有源影像轉換為金字塔TIFF檔案格式(PTIFF)。 此轉換可確保所有應用程式的映像服務的最佳運行時效能。 雖然影像伺服器可處理IC接受的所有源檔案格式，但Dynamic Media不提供此類用途的支援。

使用PTIFF檔案時，以下經驗法則可幫助您確定空間要求。

*`total_space`* （位元組）=  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* 所有原始源影像的平均像素大小（寬x高）。例如，如果原始影像通常約為2k x 2k像素，則此像素為4M像素。
* *`avg_num_components`* 視影像類型而定。對於RGB影像，大多為3，對於CMYK或RGBA影像，則為4。 如果一半影像是RGB，另一半影像是RGBA，請使用3.5。
* *`p_factor`* 取決於使用IC轉換影像時所設定的壓縮類型和質量。

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
   <td> <p>縮減壓縮 </p> </td> 
   <td> <p> 25-0.75，視影像而定 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG壓縮 </p> </td> 
   <td> <p> 1（典型的JPEG質量95） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此近似值不考慮檔案系統開銷。 磁碟上的實際空間可以大得多。

**範例**

「影像伺服」部署預計會使用30,000個低解析度的舊影像，平均大小為500x500 RGB像素。 新的打印質量影像資料預計每年以10,000的速度添加。 CMYK影像的一般大小為4k x 6k位元組。 所有資料都將以高質量壓縮JPEG。 3年使用後的磁碟空間總量估計如下：

*`total_space`* = 30,000 x(2k + 0.5k x 0.5k x 3 x 0.1)+ 3 x 10,000 x(2k + 4k x 6k x 4 x 0.1)= 2.2 G + 268 GB =約270 GB

為獲得最佳品質，可採用平縮（郵遞區號）壓縮。 假設&#x200B;*`p_factor`*&#x200B;為0.4，則所需磁碟空間總量大約是4倍。 在此情況下，略高於1 TB。
