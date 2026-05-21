---
description: 使用這些伺服器設定來重新導向錯誤。
solution: Experience Manager
title: 錯誤重新導向
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: a184e113-9708-412f-9b71-d75a35629adf
TQID: 'https://experienceleague.adobe.com/3fcob7pfE-bMms-4PtD5MKkcolKHmXEWdzEL7vgzLhc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
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
