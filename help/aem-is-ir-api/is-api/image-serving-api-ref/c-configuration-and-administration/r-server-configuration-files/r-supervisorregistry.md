---
description: 包含伺服器主管配置設定。
seo-description: 包含伺服器主管配置設定。
seo-title: SupervisorRegistry.xml
solution: Experience Manager
title: SupervisorRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 8442a3d6-5f45-48d1-8e6e-71f0ed384227
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# SupervisorRegistry.xml{#supervisorregistry-xml}

包含伺服器主管配置設定。

編輯此XML檔案時，請務必維持有效的XML語法，否則影像伺服器可能會無法啟動。

編輯完此檔案後重新啟動影像伺服，以確保您的變更生效。 僅支援以下突出顯示的元素／屬性值進行修改。 只有在Scene7技術支援建議時，才編輯此檔案的所有其他內容。

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Scene7 Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Scene7 SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Scene7 Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```

