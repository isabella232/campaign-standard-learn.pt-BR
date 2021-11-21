---
title: Etapa 2 — Integrar SDK móvel
description: Nesta parte, integraremos o aplicativo Android com o Mobile SDK. Para integrar o SDK móvel ao aplicativo Android
feature: Push
kt: 4826
doc-type: tutorial
activity: use
team: TM
exl-id: 0fa53536-8330-4e96-be2f-afc078609bcd
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# ETAPA 2 - Integrar [!UICONTROL Mobile SDK] com aplicativo Android

Nesta parte, integraremos a [!DNL Android] aplicativo com [!UICONTROL Mobile SDK]. Para integrar [!UICONTROL mobile SDK] com o [!DNL Android] aplicativo, siga as seguintes etapas:

* Abra o *ACSPushTutorial* projeto em [!DNL Android Studio]
* Crie uma nova classe java chamada *MainApp* que abrange [!DNL android.app.Application]
* A estrutura do projeto neste ponto deve ser parecida com abaixo

![aplicativo principal](assets/android-main-app.PNG)

* Expanda o [!DNL Gradle Scripts] pasta. Clique duas vezes na [!DNL build.gradle] do módulo. Cole as seguintes dependências no na seção de dependências do [!DNL build.gradle] arquivo. Seu [!DNL build.gradle] O arquivo deve ter a aparência abaixo

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![gradle de módulo](assets/module-build-gradle.PNG)

* Sincronize seu [!DNL Android] ao clicar no botão sincronizar agora para sincronizar o projeto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abrir *AndroidManifest.xml* e cole as 2 linhas a seguir após o elemento manifest e antes do elemento application . Isso permite que seu aplicativo se comunique com o mundo exterior

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copie a linha a seguir no elemento do aplicativo
[!DNL android:name=".MainApp"]
Salve as [!DNL AndroidManifest.xml]
Seu [!DNL AndroidManifest.xml] deve parecer assim

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
