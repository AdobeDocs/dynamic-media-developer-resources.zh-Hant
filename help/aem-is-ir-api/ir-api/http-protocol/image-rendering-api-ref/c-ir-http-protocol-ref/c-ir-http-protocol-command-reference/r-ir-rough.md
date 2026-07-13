---
title: 粗糙
description: 材料表面粗糙度。 指定材料曲面的相對粗糙度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 1%

---

# 粗糙{#rough}

材料表面粗糙度。 指定材料曲面的相對粗糙度。

` rough= *`值`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>表面粗糙度(0...100%)或–1，以選取預設粗糙度。 </p> </td> 
 </tr> 
</table>

用來控制3D反射演算效果。 較低的粗糙度值通常會產生更平滑的反射效果；較高的值會導致反射影像的隨機化和散射。

每個材料型別(`type=`)都根據粗糙度定義最小和最大反射演算效果。 對於某些材料型別（例如牆紙），`rough=`對於反射外觀的影響很小，而對於其他材料型別（例如石材或陶瓷），效果則明顯更明顯。

`rough=-1`將粗糙度設定為伺服器內部的預設值（一般材料型別的40%）。

## 屬性 {#section-515375758b254c80af576271bdb61bb8}

材質屬性。 如果暈映沒有3D反射功能、目標物件沒有與其關聯的3D幾何，或目標物件沒有在場景中反射任何其他物件，則忽略該暈映。

## 預設 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness`如果資料是以目錄專案為基礎，否則大約為40%。

## 另請參閱 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[型別=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ， [光澤=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)

