---
description: 使用這些伺服器設定來重定向錯誤。
solution: Experience Manager
title: 重定向錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 重定向錯誤{#error-redirection}

使用這些伺服器設定來重定向錯誤。

>[!NOTE]
>
>錯誤重定向不支援網路路徑中的垂直號字元(|)。

## PS::errorRedirect.rootUrl — 重新導向伺服器 {#section-85f22e48d68842a490b0e1191543b558}

根URL([!DNL HTTP:// *[!DNL domain]*[:*[!DNL port]*])，若次映像服務部署的請求在本地失敗，則應將其重定向。 當此設定為空或未定義時，會停用重新導向（預設）錯誤。

## PS::errorRedirect.connectTimeout — 重新導向連線逾時 {#section-3971be8f720d4b32a2cc7860b4085971}

伺服器將等待與次伺服器建立連接的最大時間（以毫秒為單位），然後將錯誤返回給客戶端。

## PS::errorRedirect.socketTimeout — 重定向響應超時 {#section-69d8579f748d4044bca99dfb64dd523c}

伺服器在丟棄重新導向請求並將錯誤傳回給用戶端之前，將等待次要伺服器傳回資料的最長時間（以毫秒為單位）。
