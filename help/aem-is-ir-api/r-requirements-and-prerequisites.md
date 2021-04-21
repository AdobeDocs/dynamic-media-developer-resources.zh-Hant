---
description: 在使用Dynamic Media影像服務之前，請確保您的系統滿足系統要求。
solution: Experience Manager
title: 系統需求和先決條件
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---


# 系統要求和先決條件{#system-requirements-and-prerequisites}

在使用Dynamic Media影像服務之前，請確保您的系統滿足系統要求。

## 伺服器硬體{#section-f3c14a7bc1b745118602659628df779f}

您的伺服器應滿足以下硬體要求。

>[!NOTE]
>
>配備AMD64和英特爾® EM64T處理器的系統通常配置為NUMA（非統一記憶體體系結構）平台。 這意味著內核在引導時構建多個記憶體節點，而不是構建單個記憶體節點。 該多節點結構可導致在其它節點耗盡之前在一個或多個節點上耗盡儲存器。 當記憶體耗盡時，內核可以決定中止進程（例如，映像伺服器或平台伺服器），即使有可用記憶體。 因此，Adobe Systems建議，如果運行這樣的系統，請關閉NUMA。 使用`numa=off`啟動選項可避免內核停止這些進程。

**Windows**

* Intel Xeon®或AMD® Opteron CPU至少具有4個內核。
* 至少16GB的記憶體。
* 交換空間至少等於物理記憶體(RAM)的兩倍。
* 2 GB的可用硬碟空間以進行安裝和基本作業，而來源影像、記錄檔、資料快取和資訊清單檔案則需要額外的磁碟空間。
* 快速乙太網網卡。

**Linux**

* Intel Xeon®或AMD® Opteron CPU至少具有4個內核。
* 至少16GB的記憶體。
* 已停用交換（建議）。
* 2 GB的可用硬碟空間以進行安裝和基本作業，而來源影像、記錄檔、資料快取和資訊清單檔案則需要額外的磁碟空間。
* 快速乙太網網卡。

**注意(Linux):** 啟用SELinux後，影像伺服無法運作。預設會啟用此選項。 要禁用SELinux，請編輯[!DNL /etc/selinux/config]檔案並將SELinux值從：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 請確定伺服器的主機名可解析為IP地址。如果不可能，請將完全限定的主機名和IP地址添加到[!DNL /etc/hosts] ，如下例所示。

`<ip address> <fully qualified hostname>`

## 伺服器軟體{#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media映像服務需要以下伺服器軟體。

**Windows**

* Microsoft® Windows 2008 Server。
* 64位元作業系統。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更新版本，以及最新的修正修補程式。
* 64位元作業系統。

**注意：** 若要在Windows上使用Image Serving，您必須安裝Microsoft Visual Studio 2010可重新散發。可在以下位置重新分發：

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

