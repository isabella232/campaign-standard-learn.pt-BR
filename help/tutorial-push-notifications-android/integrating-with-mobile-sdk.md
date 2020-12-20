---
title: Etapa 2 – Integrar SDK móvel
description: Nesta parte, integraremos o aplicativo Android ao Mobile SDK. Para integrar o SDK móvel ao aplicativo Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# ETAPA 2 - Integrar [!UICONTROL Mobile SDK] ao aplicativo Android

Nesta parte, integraremos o aplicativo [!DNL Android] com [!UICONTROL Mobile SDK]. Para integrar [!UICONTROL mobile SDK] ao aplicativo [!DNL Android], siga as seguintes etapas:

* Abra o projeto *ACSPushTutorial* em [!DNL Android Studio]
* Crie uma nova classe java chamada *MainApp* que estende [!DNL android.app.Application]
* Sua estrutura de projeto neste ponto deve ser parecida com a seguinte

![aplicativo principal](assets/android-main-app.PNG)

* Expanda a pasta [!DNL Gradle Scripts]. Duplo clique em [!DNL build.gradle] do módulo. Cole as seguintes dependências na seção dependências do arquivo [!DNL build.gradle]. Seu arquivo [!DNL build.gradle] agora deve parecer com o seguinte

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![classe de módulo](assets/module-build-gradle.PNG)

* Sincronize seu projeto [!DNL Android] clicando no botão Sincronizar agora para sincronizar seu projeto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abra *AndroidManifest.xml* e cole as seguintes 2 linhas após o elemento manifest e antes do elemento application. Isso permite que seu aplicativo se comunique com o mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copiar a seguinte linha no elemento do aplicativo
[!DNL android:name=".MainApp"]
Salve [!DNL AndroidManifest.xml]
Seu [!DNL AndroidManifest.xml] deve ter esta aparência

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
