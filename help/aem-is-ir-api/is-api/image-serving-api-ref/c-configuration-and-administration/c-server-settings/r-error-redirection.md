---
description: 使用這些伺服器設定重定向錯誤。
solution: Experience Manager
title: 重定向錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# 重定向錯誤{#error-redirection}

使用這些伺服器設定重定向錯誤。

>[!NOTE]
>
>網路路徑中的管道字元(|)不支援錯誤重定向。

## PS::errorRedirect.rootUrl — 重定向伺服器 {#section-85f22e48d68842a490b0e1191543b558}

根URL( [!DNL HTTP:// *[!DNL domain]*[: *[!DNL port]*]])用於次映像服務部署，應將本地失敗的請求重定向到該部署。 當此設定為空或未定義時，將禁用錯誤重定向（預設）。

## PS::errorRedirect.connectTimeout — 重定向連接超時 {#section-3971be8f720d4b32a2cc7860b4085971}

伺服器將等待與從屬伺服器建立連接的最長時間（以毫秒為單位），然後再將錯誤返回給客戶端。

## PS::errorRedirect.socketTimeout — 重定向響應超時 {#section-69d8579f748d4044bca99dfb64dd523c}

伺服器將在放棄重定向請求並將錯誤返回到客戶端之前等待從屬伺服器返回資料的最長時間（以毫秒為單位）。
