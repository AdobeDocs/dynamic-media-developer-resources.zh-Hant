---
title: 系統需求和先決條件
description: 在使用Dynamic Media影像伺服之前，請確定您的系統符合系統需求。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 1%

---

# 系統需求和先決條件{#system-requirements-and-prerequisites}

在使用Dynamic Media影像伺服之前，請確定您的系統符合系統需求。

## 伺服器硬體 {#section-f3c14a7bc1b745118602659628df779f}

您的伺服器應符合下列硬體需求。

>[!NOTE]
>
>處理器搭載AMD64和Intel® EM64T的系統通常設定為NUMA （非統一記憶體架構）平台。 這表示核心會在開機時建構多個記憶體節點，而不是建構單一記憶體節點。 多節點結構可能會導致一或多個節點的記憶體耗盡，之後其他節點就會耗盡。 當記憶體耗竭時，核心可以決定終止處理作業(例如，影像伺服器或 [!DNL Platform Server])即使有可用的記憶體。 因此，Adobe建議，如果您正在執行這樣的系統，請關閉NUMA。 使用 `numa=off` 啟動選項，可避免核心停止這些處理程式。

**Windows**

* Intel Xeon®或AMD® Opteron CPU，至少配備四個核心。
* 最少1 GB的RAM。
* 交換空間至少相當於實體記憶體(RAM)容量的兩倍。
* 2 GB的可用硬碟空間可供安裝及基本作業使用，來源映像、記錄、資料快取及資訊清單檔案需要額外的磁碟空間。
* 快速乙太網路介面卡。

**Linux®**

* Intel Xeon®或AMD® Opteron CPU，至少配備四個核心。
* 最少16 GB的RAM。
* 已停用交換（建議）。
* 2 GB的可用硬碟空間可供安裝及基本作業使用，來源映像、記錄、資料快取及資訊清單檔案需要額外的磁碟空間。
* 快速乙太網路介面卡。

**注意(Linux®)：** 開啟SELinux時，「影像伺服」無法運作。 此選項預設為啟用。 若要停用SELinux，請編輯 [!DNL /etc/selinux/config] 檔案並將SELinux值從下列位置變更：

`SELINUX=enforcing`

收件者

`SELINUX=disabled`

**注意(Linux®)：** 請確定伺服器的主機名稱可解析為IP位址。 如果無法執行此操作，請將完整主機名稱和IP位址新增至 [!DNL /etc/hosts] 如下列範例所示。

`<ip address> <fully qualified hostname>`

## 伺服器軟體 {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving需要下列伺服器軟體。

**Windows**

* Microsoft® Windows Server 2008。
* 64位元作業系統。

**Linux®**

* Red Hat® Enterprise 5或CentOS 5.5和更新版本，搭配最新的修正修補程式。
* 64位元作業系統。

**注意：** 若要在Windows上使用影像伺服，您必須安裝Microsoft® Visual Studio 2010。
