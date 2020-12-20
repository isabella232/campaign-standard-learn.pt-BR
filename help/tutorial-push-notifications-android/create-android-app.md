---
title: Etapa 1 - Criar aplicativo Android e configurar para usar o Firebase Cloud Messaging
description: Nesta parte, criaremos [!DNL Android] App to receive [!UICONTROL Push notifications] enviado da Adobe Campaign Standard. Para receber as notificações por push, o aplicativo precisa ser registrado com o Google [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: cdd78e97f2769503d3d4f26933ccc7f35e9b20b9
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---


# Etapa 1 - Criar [!DNL Android] aplicativo e configurar para usar [!DNL Firebase Cloud Messaging]

Nesta parte, você criará o aplicativo [!DNL Android] para receber [!UICONTROL Push notifications] enviado da Adobe Campaign Standard. Para receber as notificações por push, o aplicativo precisa ser registrado com o [!DNL Firebase Cloud Service] do Google.

1. Faça logon em sua conta [!DNL Firebase].

   [!DNL Firebase] é a plataforma móvel do Google que ajuda você a desenvolver rapidamente aplicativos de alta qualidade. Se você não tiver uma conta [!DNL Firebase], crie uma [daqui](https://firebase.google.com).

2. Iniciar [!DNL Android Studio]
3. Clique em **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selecione **[!UICONTROL Empty Activity]** e clique em **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Forneça um nome significativo para o projeto.

   Para o objetivo desta demonstração, nós nomeamos nosso projeto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Aceite os nomes de pacote padrão e clique em **[!DNL Finish]** para criar seu projeto.
7. A estrutura do projeto deve ser semelhante à captura de tela abaixo

   ![android-project-structure](assets/android-project-structure.PNG)

8. Clique em **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (isso adiciona o projeto ao  [!DNL Firebase])
9. Clique em **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![firebase de configuração](assets/android-project-firebase-messaging.PNG)

10. Clique em **[!UICONTROL Connect to Firebase].**
11. Depois que o aplicativo estiver conectado ao Firebase, clique em **[!UICONTROL Add FCM to your app].**
12. Clique em **[!UICONTROL Accept Changes].**

   Ao adicionar o FCM ao seu aplicativo, o assistente precisa de sua permissão para fazer algumas alterações no seu projeto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Na integração bem-sucedida de seu aplicativo com o Firebase, você deve receber uma mensagem como a mostrada abaixo:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Verifique se o projeto está listado  [!DNL Firebase ]no console](https://console.firebase.google.com/)

## Configurar [!UICONTROL Push Channel] Definições

1. Faça logon no console [!DNL Firebase]
2. Abra o projeto **[!UICONTROL ACSPushTutorial]**.
3. Clique no ícone **engrenagem** e abra as configurações do projeto

   ![project-settings](assets/firebase-project-settings.PNG)

4. Pressione para a guia **[!UICONTROL Cloud Messaging]**.
5. Copiar a chave do servidor

   ![chave de servidor](assets/firebase-server-key.PNG)

6. Faça logon em sua instância do Adobe Campaign Standard
7. Clique em **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selecione o **[!UICONTROL Mobile Application Property]apropriado.**
9. Clique no ícone **[!DNL Android]** na seção **[!UICONTROL Push Channel settings]**.
10. Cole a chave do servidor no campo da chave do servidor.

Se tudo correr bem, você deverá ver uma mensagem de sucesso.

![configurações de canal de push](assets/push-channel-settings.PNG)

Para resumir, criamos um [!DNL Android App] e conectamos o [!DNL Android App] ao [!DNL Firebase]. Em seguida, conectamos o aplicativo móvel no Adobe Campaign com o [!DNL Android App] colando a chave do servidor do aplicativo [!DNL Android] no aplicativo móvel no Adobe Campaign Standard.
