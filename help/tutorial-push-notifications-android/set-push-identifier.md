---
title: ETAPA 4 - Definir identificador de push
description: O **pushIdentifier** é uma string que contém o token do dispositivo para notificações por push. Esse é o mesmo token enviado pelo Firebase e passado para o SDK usando o método MobileCore.setPushIdentifier.
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Etapa 4 - Definir [!DNL pushidentifier]

A **[!DNL pushidentifier]** é uma string que contém o token do dispositivo para [!DNL Push] notificações. Esse é o mesmo token enviado por [!DNL Firebase] e passado para o SDK usando o [!DNL MobileCore.setPushIdentifier] método.

Abra seu projeto no [!DNL Android ]estúdio. Exclua o código inteiro em [!DNL MainActivity] exceto a primeira linha que é a declaração **** do pacote.

Cole o seguinte código em [!DNL MainActivity]:

```java{.line-numbers}
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Teste seu aplicativo

Agora é uma boa hora para testar seu aplicativo, antes de ir mais longe.

* Execute seu aplicativo clicando em seta verde ou selecione **[!DNL Run->Run'app']**.
* O [!DNL Android] emulador deve ser start e você deve ver seu aplicativo sendo executado com [!DNL "Hello World" ]texto.
* Abra a [!DNL logcat] janela. Procure &quot;[!DNL Got]&quot;. Você deve ver o token que foi recebido de [!DNL Firebase] gravado no log, como mostrado abaixo. A string longa após &quot;[!DNL Got token]&quot; é a [!DNL pushidentifier ]que é enviada para Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Verificar assinantes do aplicativo móvel

Faça logon na sua instância do Adobe Campaign Standard.
Navegue **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Abra o aplicativo móvel apropriado. Pressione até a [!UICONTROL Mobile Application Subscribers] guia. Você deve ver uma [!UICONTROL registration token ]lista.

![assinantes de aplicativos móveis](assets/mobile-application-subscribers.PNG)

>[OBSERVAÇÃO]
>Se você não vir o token de registro na guia [!UICONTROL Mobile Application Subscribers] PARE aqui antes de continuar.
