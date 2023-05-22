---
description: 本節包含針對影像服務偶爾出現的問題的解決方案。
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

本節包含針對影像服務偶爾出現的問題的解決方案。

**一般**

ImageServer現在保留安裝日誌和升級安裝過程中更改的所有檔案的備份資料夾。 此檔案和資料夾可在Image Service安裝目錄的根目錄下找到。

**啟動映像伺服器時，啟動指令碼將停止顯示消息「啟動掛起」（僅限LINUX）**

這可能表示映像服務許可證有問題，例如缺少許可證檔案或臨時許可證過期。 有效的許可證檔案必須位於 [!DNL /usr/local/scene7/licenses]。

**映像伺服器停止或崩潰，並且映像伺服器日誌檔案指示檔案中的空間不足或資源暫時不可用 [!DNL IgcVirtualMemory.cpp]&quot;**

此錯誤消息的原因是映像伺服器未能分配配置為使用的記憶體量。

* 在中檢查物理記憶體設定 [!DNL ImageServerRegistry.xml]。 它不應超過50%，如果其他記憶體密集型應用程式在同一系統上運行，則應低於50%。 預設為20%。
* 確保伺服器上的交換空間至少是物理RAM的兩倍。 交換空間設定不足可導致此問題。

**快取資料夾使用的實際磁碟空間超過 ` *[!DNL cache.maxSize]*`設定[!DNL PlatformServer.conf]**

這不表示有問題。 檔案系統開銷未包含在 [!DNL Platform Server]磁碟快取設定。 系統報告的總量可大大高於設定。 建議保留兩倍於中指定的磁碟空間 ` *[!DNL cache.maxSize]*`。

**is-docs示例中的損壞影像**

如果映像伺服器未運行，則會發生此情況。 如果目錄根路徑或映像根路徑已從安裝預設值更改，但示例映像和目錄尚未移動到新位置，則還會出現這種情況。 檢查配置檔案中的Image Server根路徑值。 如有必要，將包含示例影像的演示資料夾移到當前影像根目錄，然後移動 [!DNL sample*.*] 到當前目錄根目錄。

示例還假定 [!DNL default.ini] 為標準（例如，不能啟用混淆或鎖定）。

**在大量正常運行後，快取未命中過多**

根據伺服器使用情況，通過提高 [!DNL Platform Server] 磁碟快取大小（如果磁碟空間可用）。 可以通過手動編輯配置檔案來更改設定。 請參閱文檔。

**日誌檔案佔用的磁碟空間過多**

映像伺服器和 [!DNL Platform Server] 每天啟動新日誌檔案。 預設情況下，這些內容會放在[!DNL]中 *[!DNL install_root]*/ImageServing/logs]。 可以配置日誌檔案大小、保留的日誌數和日誌內容。 請參閱文檔。

**如果伺服器上安裝了防病毒軟體**

建議關閉對Image Serving目錄的掃描。 否則，掃描高容量讀/寫目錄（如快取、影像、字型、配置檔案和目錄目錄）將導致問題。

**Digimarc導致縮放影像的效能問題**

不要在縮放的影像上使用Digimarc。 效能不可接受。 如有必要，請為要用於縮放的影像建立單獨的目錄，並禁用此目錄的Digimarc。
