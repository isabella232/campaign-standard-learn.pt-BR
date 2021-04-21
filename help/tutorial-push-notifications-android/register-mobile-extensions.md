---
title: Etapa 3 - Registrar extensões no aplicativo móvel
description: Nesta parte, adicionaremos o código para registrar as extensões UserProfile, Identity, Lifecycle e Signal.
feature: Push
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 12%

---

# Etapa 3 - Registrar extensões no aplicativo móvel

Nessa parte, adicionaremos o código para registrar as extensões Perfil de usuário, Identidade, Ciclo de vida e Sinal. Essas extensões fazem parte de [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Também precisaremos registrar a extensão Adobe Campaign Standard, conforme mostrado no código abaixo.

Abra o projeto no estúdio [!DNL Android]. Exclua o código inteiro em MainApp **exceto a primeira linha que é a instrução do pacote**.

Cole o seguinte código no MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Na linha 32, você precisa fornecer a id do arquivo de ambiente da propriedade [!UICONTROL  Launch]. Isso pode ser acessado a partir de [!UICONTROL environment tab] da propriedade [!UICONTROL Launch].

![launch-id](assets/launch-id-property.PNG)
