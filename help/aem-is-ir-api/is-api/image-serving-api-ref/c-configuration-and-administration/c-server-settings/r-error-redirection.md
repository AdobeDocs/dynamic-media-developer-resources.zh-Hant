---
description: 使用這些伺服器設定來重新導向錯誤。
solution: Experience Manager
title: 錯誤重新導向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# 錯誤重新導向{#error-redirection}

使用這些伺服器設定來重新導向錯誤。

>[!NOTE]
>
>網路路徑中的管路字元(|)不支援錯誤重新導向。

## PS：：errorRedirect.rootUrl — 重新導向伺服器 {#section-85f22e48d68842a490b0e1191543b558}

應該將本機失敗之要求的次要影像伺服部署根URL ( HTTP:// *[!DNL domain]*[: *[!DNL port]*])重新導向。 此設定為空白或未定義時，錯誤重新導向功能會停用（預設）。

## PS：：errorRedirect.connectTimeout — 重新導向連線逾時 {#section-3971be8f720d4b32a2cc7860b4085971}

伺服器等待與次要伺服器建立連線的最長時間（以毫秒為單位），之後才會傳回錯誤給使用者端。

## PS：：errorRedirect.socketTimeout — 重新導向回應逾時 {#section-69d8579f748d4044bca99dfb64dd523c}

伺服器等待次要伺服器傳回資料的最長時間（以毫秒為單位），之後會放棄重新導向要求並將錯誤傳回使用者端。
