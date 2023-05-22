---
description: 使用Dynamic Media映像服務之前，請確保您的系統符合系統要求。
solution: Experience Manager
title: 系統要求和先決條件
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 1%

---

# 系統要求和先決條件{#system-requirements-and-prerequisites}

使用Dynamic Media映像服務之前，請確保您的系統符合系統要求。

## 伺服器硬體 {#section-f3c14a7bc1b745118602659628df779f}

伺服器應滿足以下硬體要求。

>[!NOTE]
>
>帶有AMD64和英特爾® EM64T處理器的系統通常配置為NUMA（非統一記憶體體系結構）平台。 這意味著內核在引導時構建多個記憶體節點，而不是構建單個記憶體節點。 該多節點構造可導致在其它節點耗盡之前在一個或多個節點上耗盡記憶體。 當記憶體耗盡時，內核可以決定終止進程(例如，映像伺服器或 [!DNL Platform Server])，即使有可用記憶體。 因此，Adobe Systems建議，如果運行這樣的系統，則關閉NUMA。 使用 `numa=off` start選項可避免內核停止這些進程。

**Windows**

* 至少具有4個內核的英特爾至強®或AMD皓龍CPU。
* 最小16GB RAM。
* 交換空間至少等於物理記憶體(RAM)的兩倍。
* 2 GB可用硬碟空間用於安裝和基本操作，源映像、日誌、資料快取和清單檔案需要額外的磁碟空間。
* 快速乙太網網卡。

**Linux**

* 至少具有4個內核的英特爾至強®或AMD皓龍CPU。
* 最小16GB RAM。
* 已禁用交換（建議）。
* 2 GB可用硬碟空間用於安裝和基本操作，源映像、日誌、資料快取和清單檔案需要額外的磁碟空間。
* 快速乙太網網卡。

**注意(Linux):** 開啟SELinux時，影像服務不工作。 預設情況下，此選項處於啟用狀態。 要禁用SELinux，請編輯 [!DNL /etc/selinux/config] 檔案，並將SELinux值從：

`SELINUX=enforcing`

至

`SELINUX=disabled`

**注意(Linux):** 確保伺服器的主機名可解析為IP地址。 如果不可能，請將完全限定的主機名和IP地址添加到 [!DNL /etc/hosts] 如下例所示。

`<ip address> <fully qualified hostname>`

## 伺服器軟體 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media映像服務需要以下伺服器軟體。

**Windows**

* Microsoft® Windows 2008伺服器。
* 64位作業系統。

**Linux**

* Red Hat® Enterprise 5或CentOS 5.5及更高版本，帶有最新的修復補丁程式。
* 64位作業系統。

**注：** 要在Windows上使用Image Serving，必須安裝MicrosoftVisual Studio 2010可再發行版。
