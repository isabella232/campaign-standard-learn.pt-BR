---
title: Etapa 2 - Integração do SDK móvel
description: Nesta parte, integraremos o aplicativo Android ao Mobile SDK. Para integrar o SDK móvel ao aplicativo Android
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# ETAPA 2 - Integrar [!UICONTROL Mobile SDK] ao aplicativo Android

Nesta parte, integraremos o [!DNL Android] aplicativo com [!UICONTROL Mobile SDK]. Para fazer a integração [!UICONTROL mobile SDK] com o [!DNL Android] aplicativo, siga as seguintes etapas:

* Abra o projeto *ACSPushTutorial* em [!DNL Android Studio]
* Crie uma nova classe java chamada *MainApp* , que se estende [!DNL android.app.Application]
* Sua estrutura de projeto neste ponto deve ser parecida com a seguinte

![aplicativo principal](assets/android-main-app.PNG)

* Expanda a [!DNL Gradle Scripts] pasta. Clique no Duplo [!DNL build.gradle] do módulo. Cole as seguintes dependências na seção dependências do [!DNL build.gradle] arquivo. Seu [!DNL build.gradle] arquivo agora deve ter a aparência abaixo

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![classe de módulo](assets/module-build-gradle.PNG)

* Sincronize seu [!DNL Android] projeto clicando no botão Sincronizar agora para sincronizar seu projeto

## Modificar [!DNL AndroidManifest.xml]{#modify-android-manifest}

Abra *AndroidManifest.xml* e cole as duas linhas a seguir depois do elemento manifest e antes do elemento application. Isso permite que seu aplicativo se comunique com o mundo exterior

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Copie a linha a seguir no elemento[!DNL android:name=".MainApp"]do aplicativoSalve [!DNL AndroidManifest.xml]sua [!DNL AndroidManifest.xml] aparência

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
