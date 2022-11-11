---
description: 本節包含偶爾與「影像伺服」一起發生的問題的解決方案。
solution: Experience Manager
title: 疑難排解
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 疑難排解{#troubleshooting}

本節包含偶爾與「影像伺服」一起發生的問題的解決方案。

**一般**

ImageServer現在會保留安裝日誌和在升級安裝期間更改的所有檔案的備份資料夾。 此檔案和資料夾可在映像服務安裝目錄的根目錄中找到。

**啟動映像伺服器時，啟動指令碼會與消息「啟動掛起」（僅限LINUX）停頓**

這可能表示映像服務許可證出現問題，例如缺少許可證檔案或臨時許可證已過期。 有效的許可證檔案必須位於 [!DNL /usr/local/scene7/licenses].

**映像伺服器中斷或崩潰，且映像伺服器日誌檔案指示空間不足或「檔案中資源暫時不可用」 [!DNL IgcVirtualMemory.cpp]&quot;**

此錯誤消息的原因是映像伺服器未能分配其配置為使用的記憶體量。

* 檢查中的「Physical Memory（物理記憶體）」設定 [!DNL ImageServerRegistry.xml]. 它不應超過50%，如果其他記憶體密集型應用程式在同一系統上運行，它應該會更少。 預設為20%。
* 確保伺服器上的交換空間至少是物理RAM的兩倍。 交換空間設定低可能導致此問題。

**快取資料夾使用的實際磁碟空間超過 ` *[!DNL cache.maxSize]*`設定[!DNL PlatformServer.conf]**

這不表示有問題。 檔案系統開銷不包含在 [!DNL Platform Server]的磁碟快取設定。 由系統報告的總量可以大於設定。 建議保留的磁碟空間是 ` *[!DNL cache.maxSize]*`.

**is-docs範例中的影像損毀**

如果映像伺服器未運行，則會發生此情況。 如果目錄根路徑或映像根路徑已從安裝預設值更改，但示例映像和目錄尚未移到新位置，則也會發生此情況。 檢查配置檔案中的「映像伺服器根路徑」值。 如有必要，將包含範例影像的示範資料夾移至目前的影像根目錄，然後移動 [!DNL sample*.*] 到當前目錄根目錄。

範例也假設 [!DNL default.ini] 為標準（例如不得啟用模糊化或鎖定）。

**大量正常運行時間後，太多快取丟失**

根據伺服器使用情況，可通過提高 [!DNL Platform Server] 磁碟快取大小（如果磁碟空間可用）。 您可以手動編輯組態檔來變更設定。 請參閱檔案。

**日誌檔案佔用的磁碟空間過多**

影像伺服器和 [!DNL Platform Server] 每天啟動新日誌檔案。 依預設，這些會放在[!DNL中 *[!DNL install_root]*/ImageServing/logs]。 可以配置日誌檔案大小、保留的日誌數和日誌內容。 請參閱檔案。

**如果伺服器上安裝了防病毒軟體**

建議您關閉對映像伺服目錄的掃描。 否則，掃描高卷讀/寫目錄（如快取、影像、字型、配置檔案和目錄）將導致問題。

**Digimarc導致縮放影像的效能問題**

請勿在縮放的影像上使用Digimarc。 無法接受此效能。 如有必要，請為要用於縮放和停用此目錄的Digimarc的影像建立個別目錄。
