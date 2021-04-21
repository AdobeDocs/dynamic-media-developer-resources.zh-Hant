---
description: 本節包含影像伺服偶爾發生之問題的解決方案。
solution: Experience Manager
title: 疑難排解
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---


# 疑難排解{#troubleshooting}

本節包含影像伺服偶爾發生之問題的解決方案。

**一般**

ImageServer現在會保留安裝日誌和升級安裝期間更改的所有檔案的備份資料夾。 此檔案和資料夾可以在Image Serving安裝目錄的根目錄中找到。

**啟動映像伺服器時，啟動指令碼將停止顯示消息「啟動暫掛」（僅限LINUX）**

這可能表示影像伺服授權有問題，例如遺失授權檔案或過期的臨時授權。 有效的許可證檔案必須位於[!DNL /usr/local/scene7/licenses]中。

**Image Server停止或當機，而Image Server日誌檔案指示空間不足或「檔案中暫時不可用的資源 [!DNL IgcVirtualMemory.cpp]」**

此錯誤消息的原因是映像伺服器未能分配配置為使用的記憶體量。

* 檢查[!DNL ImageServerRegistry.xml]中的「Physical Memory（物理記憶體）」設定。 它不應超過50%，如果在同一系統上運行其他記憶體密集型應用程式，則應該更低。 預設值為20%。
* 確保伺服器上的交換空間至少是物理RAM的兩倍。 交換空間設定不足可能導致此問題。

**快取資料夾使用的實際磁碟空間超過 ` *[!DNL cache.maxSize]*`在[!DNL PlatformServer.conf]**

這不表示有問題。 平台伺服器的磁碟快取設定中不包括檔案系統開銷。 由系統報告的總量可大大高於設定。 建議保留的磁碟空間是` *[!DNL cache.maxSize]*`中指定的兩倍。

**is-docs範例中的損毀影像**

如果映像伺服器未運行，則會發生此情況。 如果目錄根路徑或映像根路徑已從安裝預設值更改，但示例映像和目錄尚未移動到新位置，則也會發生這種情況。 檢查配置檔案中的「映像伺服器根路徑」值。 如有必要，將包含範例影像的示範檔案夾移至目前的影像根目錄，並將[!DNL sample*.*]移至目前的目錄根目錄。

範例也假設[!DNL default.ini]中的某些設定為標準（例如，不得啟用模糊化或鎖定）。

**在長時間運行後發生過多快取丟失**

視伺服器使用情況而定，如果有可用磁碟空間，則可增加平台伺服器磁碟快取大小，以改善效能。 可以手動編輯配置檔案來更改設定。 請參閱檔案。

**日誌檔案佔用的磁碟空間過多**

映像伺服器和平台伺服器每天都啟動一個新日誌檔案。 預設情況下，這些檔案放在[!DNL *[!DNL install_root]*/ImageServing/logs]中。 日誌檔案大小、保留的日誌數以及可以配置的日誌內容。 請參閱檔案。

**如果您的伺服器上安裝了防病毒軟體**

建議您關閉「影像服務」目錄的掃描。 否則，掃描大量讀／寫目錄（如快取、影像、字型、配置檔案和目錄目錄）將會導致問題。

**Digimarc造成縮放影像的效能問題**

請勿在將縮放的影像上使用Digimarc。 無法接受此效能。 如有必要，請為要用於縮放的影像建立個別目錄，並停用此目錄的Digimarc。
