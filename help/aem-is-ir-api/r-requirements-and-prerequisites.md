---
description: 使用Dynamic Media Image Serving之前，請確保您的系統符合系統要求。
solution: Experience Manager
title: 系統需求和先決條件
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 1%

---

# 系統需求和先決條件{#system-requirements-and-prerequisites}

使用Dynamic Media Image Serving之前，請確保您的系統符合系統要求。

## 伺服器硬體 {#section-f3c14a7bc1b745118602659628df779f}

您的伺服器應滿足以下硬體要求。

>[!NOTE]
>
>具有AMD64和英特爾® EM64T處理器的系統通常配置為NUMA（非統一記憶體架構）平台。 這意味著內核在啟動時構建多個記憶體節點，而不是構建單個記憶體節點。 該多節點結構可導致在一個或多個節點耗盡之前對其它節點耗盡記憶體。 當記憶體耗盡時，內核可以決定終止進程（例如，映像伺服器或平台伺服器），即使記憶體可用。 因此，Adobe Systems建議，如果運行這樣的系統，則關閉NUMA。 使用`numa=off`啟動選項來避免內核停止這些進程。

**Windows**

* 至少具有4個內核的英特爾至強®或AMD®皓龍CPU。
* 最少16GB記憶體。
* 交換空間至少等於物理記憶體(RAM)量的兩倍。
* 2 GB的可用硬碟空間用於安裝和基本操作，源映像、日誌、資料快取和清單檔案需要額外的磁碟空間。
* 快速乙太網網路介面卡。

**Linux**

* 至少具有4個內核的英特爾至強®或AMD®皓龍CPU。
* 最少16GB記憶體。
* 禁用交換（建議）。
* 2 GB的可用硬碟空間用於安裝和基本操作，源映像、日誌、資料快取和清單檔案需要額外的磁碟空間。
* 快速乙太網網路介面卡。

**注意(Linux):** 開啟SELinux時影像伺服無法運作。預設會啟用此選項。 要禁用SELinux，請編輯[!DNL /etc/selinux/config]檔案，並將SELinux值從：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 請確定伺服器的主機名稱可解析為IP位址。如果不能，請按照以下示例將完全限定的主機名和IP地址添加到[!DNL /etc/hosts]中。

`<ip address> <fully qualified hostname>`

## 伺服器軟體 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving需要下列伺服器軟體。

**Windows**

* Microsoft® Windows 2008 Server。
* 64位作業系統。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更新版本，以及最新的修正修補程式。
* 64位作業系統。

**注意：** 若要在Windows上使用影像伺服，您必須安裝Microsoft Visual Studio 2010可重新分發。可再分派之地點如下：

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)
