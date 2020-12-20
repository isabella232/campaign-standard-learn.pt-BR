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
source-git-commit: aa01c2f8fe1560468d0d8f3fae6291bb82f9a21f
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Etapa 4 - Definir [!DNL pushidentifier]

O **[!DNL pushidentifier]** é uma cadeia de caracteres que contém o token de dispositivo para notificações [!DNL Push]. Esse é o mesmo token enviado por [!DNL Firebase] e passado para o SDK usando o método [!DNL MobileCore.setPushIdentifier].

Abra seu projeto no estúdio [!DNL Android ]. Exclua o código inteiro em [!DNL MainActivity] **exceto a primeira linha que é a declaração do pacote**.

Cole o seguinte código em [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
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

* Execute seu aplicativo clicando na seta verde ou selecione **[!DNL Run->Run'app']**.
* O emulador [!DNL Android] deve ser start e você deve ver seu aplicativo sendo executado com [!DNL "Hello World" ]texto.
* Abra a janela [!DNL logcat]. Procure &quot;[!DNL Got]&quot;. Você deve ver o token recebido de [!DNL Firebase] gravado no log, como mostrado abaixo. A string longa depois de &quot;[!DNL Got token]&quot; é o [!DNL pushidentifier ]que é enviado para a Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Verificar assinantes do aplicativo móvel

Faça logon na sua instância do Adobe Campaign Standard.
Navegue **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Abra o aplicativo móvel apropriado. Pressione para a guia [!UICONTROL Mobile Application Subscribers]. Você deve ver um [!UICONTROL registration token ]listado.

![assinantes de aplicativos móveis](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Se você não vir o token de registro na guia [!UICONTROL Mobile Application Subscribers], PARE aqui antes de continuar.
