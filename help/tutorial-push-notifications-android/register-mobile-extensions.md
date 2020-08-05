---
title: Etapa 3 - Registrar extensões com seu aplicativo móvel
description: Nesta parte, adicionaremos o código para registrar as extensões UserProfile, Identity, Lifecycle e Signal.
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Etapa 3 - Registrar extensões com seu aplicativo móvel

Nesta parte, adicionaremos o código para registrar as extensões Perfil do usuário, Identidade, Ciclo de vida e Sinal. Essas extensões fazem parte do [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Também será necessário registrar a extensão do Adobe Campaign Standard, conforme mostrado no código abaixo.

Abra seu projeto no [!DNL Android] estúdio. Exclua o código inteiro no MainApp, **exceto a primeira linha que é a declaração** do pacote.

Cole o seguinte código no MainApp

```java{.line-numbers}
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

Linha 32, é necessário fornecer a ID do arquivo de ambiente de sua[!UICONTROL  Launch] propriedade. Isso pode ser acessado a partir [!UICONTROL environment tab] da sua [!UICONTROL Launch] propriedade.

![launch-id](assets/launch-id-property.PNG)
