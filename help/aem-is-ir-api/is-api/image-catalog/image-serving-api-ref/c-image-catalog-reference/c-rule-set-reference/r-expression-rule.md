---
description: 規則運算式模式元素。 <rule>元素中的選用專案。
solution: Experience Manager
title: 運算式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
TQID: 'https://experienceleague.adobe.com/lYaMuefBswTJcGuSm7Rm-yNTpz1UbOkjJLpdCOdXNrQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 4%

---

# 運算式{#expression}

規則運算式模式元素。 `<rule>`個元素中的選用專案。

## 屬性 {#section-2d438c889ae84b6da7e0ed84b5d021a0}

無。

## 資料 {#section-e2601008d71243109af1a8c55b58416d}

規則運算式模式字串。

## 說明 {#section-759bfb738ddb45dba1f0807aba8c1113}

`<expression>`專案可以是空的，或包含簡單的搜尋字串或規則運算式模式。 此模式會套用至整個請求字串。

當`<expression>`為空白或未指定時，一律會有相符專案；這等同於指定`<expression>.*</expression>`。

實作是以Java套件[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)為基礎，提供與Perl類似的規則運算式語法。

## 附註 {#section-10b472a902674893b49ca49a7052c366}

運算式字串不得包含常值&lt;和&amp;字元。 這些保留字元可分別以`&`和`<`編碼，或是整個字串可包含在XML `CDATA`區段中：

`<expression><![CDATA[&fmt=custom]]></expression>`

`<expression>`與`</expression>`標籤之間的所有字元都會傳遞至規則運算式剖析器，包括選擇性`CDATA`區段以外的字元。 請務必避免出現額外的空白字元。

## 另請參閱 {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
