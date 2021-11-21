---
title: ETAPA 4 - Definir identificador de push
description: O **pushIdentifier** é uma string que contém o token do dispositivo para notificações por push. É o mesmo token enviado pelo Firebase e passado para o SDK usando o método MobileCore.setPushIdentifier .
feature: Push
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 5a2f8c9a78bf5100b272f9b4461131545b3aeb8b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Etapa 4 - Definir [!DNL pushidentifier]

O **[!DNL pushidentifier]** é uma string que contém o token de dispositivo para [!DNL Push] notificações. Ele é o mesmo token enviado por [!DNL Firebase] e é passado para o SDK usando o [!DNL MobileCore.setPushIdentifier] método .

Abra o projeto em [!DNL Android™ ]estúdio. Exclua o código inteiro em [!DNL MainActivity] **exceto a primeira linha que é a declaração do seu pacote**.

Cole o código a seguir em [!DNL MainActivity]:

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

## Testar seu aplicativo

Agora é um bom momento para testar seu aplicativo, antes de prosseguir.

* Execute seu aplicativo clicando na seta verde ou selecione **[!DNL Run->Run'app']**.
* O [!DNL Android™] o emulador deve iniciar e você deve ver seu aplicativo em execução com [!DNL "Hello World" ]texto.
* Abra o [!DNL logcat] janela. Pesquisar por &quot;[!DNL Got]&quot;. Você deve ver o token recebido de [!DNL Firebase] gravado no log conforme mostrado abaixo. A sequência longa depois de &quot;[!DNL Got token]&quot; é o [!DNL pushidentifier ]que é enviado para o Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Verificar Assinantes de Aplicativos Móveis

Faça logon na instância do Adobe Campaign Standard.
Navegar **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Abra o aplicativo móvel apropriado. Guia para [!UICONTROL Mobile Application Subscribers] guia . Você deve ver um [!UICONTROL registration token ]listado.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Se você não vir o token de registro no [!UICONTROL Mobile Application Subscribers] pressione STOP aqui antes de continuar.
