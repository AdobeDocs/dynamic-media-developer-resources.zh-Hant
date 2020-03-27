---
description: 使用這些伺服器設定來重新導向錯誤。
seo-description: 使用這些伺服器設定來重新導向錯誤。
seo-title: 重定向錯誤
solution: Experience Manager
title: 重定向錯誤
topic: Scene7 Image Serving - Image Rendering API
uuid: b2c2f725-98c3-44a4-8f50-2ca4da7f2156
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 重定向錯誤{#error-redirection}

使用這些伺服器設定來重新導向錯誤。

>[!NOTE]
>
>不支援網路路徑中的垂直號字元(|)進行錯誤重新導向。

## PS::errorRedirect.rootUrl —— 重新導向伺服器 {#section-85f22e48d68842a490b0e1191543b558}

根URL([!DNL HTTP:// *[!DNL domain]*[:] *[!DNL port]*])的次映像服務部署，應將本地失敗的請求重定向到該次映像服務部署。 當此設定為空或未定義時，會停用錯誤重新導向（預設）。

## PS::errorRedirect.connectTimeout —— 重定向連接超時 {#section-3971be8f720d4b32a2cc7860b4085971}

伺服器將等待與輔助伺服器建立連接的最長時間（以毫秒為單位），然後將錯誤返回到客戶端。

## PS::errorRedirect.socketTimeout —— 重新導向回應逾時 {#section-69d8579f748d4044bca99dfb64dd523c}

伺服器在放棄重新導向要求並將錯誤傳回用戶端之前，會等候次要伺服器傳回資料的最長時間（以毫秒為單位）。
