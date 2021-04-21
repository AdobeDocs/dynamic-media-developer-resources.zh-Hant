---
description: 使用這些伺服器設定來重新導向錯誤。
solution: Experience Manager
title: 重定向錯誤
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 重定向錯誤{#error-redirection}

使用這些伺服器設定來重新導向錯誤。

>[!NOTE]
>
>不支援網路路徑中的垂直號字元(|)進行錯誤重新導向。

## PS::errorRedirect.rootUrl —— 重新導向伺服器{#section-85f22e48d68842a490b0e1191543b558}

根URL([!DNL HTTP:// *[!DNL domain]*[:*[!DNL port]*])，以部署次要影像服務，應將本機失敗的請求重新導向至該部署。 當此設定為空或未定義時，會停用錯誤重新導向（預設）。

## PS::errorRedirect.connectTimeout —— 重定向連接超時{#section-3971be8f720d4b32a2cc7860b4085971}

伺服器將等待與輔助伺服器建立連接的最長時間（以毫秒為單位），然後將錯誤返回到客戶端。

## PS::errorRedirect.socketTimeout —— 重定向響應超時{#section-69d8579f748d4044bca99dfb64dd523c}

伺服器在放棄重新導向要求並將錯誤傳回用戶端之前，會等候次要伺服器傳回資料的最長時間（以毫秒為單位）。
