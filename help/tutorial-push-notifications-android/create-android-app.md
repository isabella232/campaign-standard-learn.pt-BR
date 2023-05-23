---
title: Etapa 1 - Criação do aplicativo Android e configuração para usar o Firebase Cloud Messaging
description: Nesta parte criaremos [!DNL Android] Aplicativo a ser recebido [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Google Para receber as notificações por push, o aplicativo precisa ser registrado com o [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# Etapa 1 - Criação [!DNL Android] Aplicativo e configuração para uso [!DNL Firebase Cloud Messaging]

Nesta parte, você criará [!DNL Android] Aplicativo a ser recebido [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Google Para receber as notificações por push, o aplicativo precisa ser registrado com o [!DNL Firebase Cloud Service].

1. Faça logon no [!DNL Firebase] conta.

   [!DNL Firebase] O é a plataforma móvel da Google que ajuda você a desenvolver rapidamente aplicativos de alta qualidade. Se você não tiver uma [!DNL Firebase] conta, crie uma [daqui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Clique em **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selecione **[!UICONTROL Empty Activity]** e clique em **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Forneça um nome significativo para o projeto.

   Para o propósito desta demonstração, nomeamos nosso projeto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Aceite os nomes de pacote padrão e clique em **[!DNL Finish]** para criar seu projeto.
7. A estrutura do projeto deve ser semelhante à captura de tela abaixo

   ![android-project-structure](assets/android-project-structure.PNG)

8. Clique em **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (isso adiciona o projeto a [!DNL Firebase])
9. Clique em **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar firebase](assets/android-project-firebase-messaging.PNG)

10. Clique em **[!UICONTROL Connect to Firebase].**
11. Depois que seu aplicativo estiver conectado ao Firebase, clique em **[!UICONTROL Add FCM to your app].**
12. Clique em **[!UICONTROL Accept Changes].**

   Quando você está adicionando o FCM ao aplicativo, o assistente precisa de sua permissão para fazer algumas alterações no projeto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Ao integrar com êxito seu aplicativo ao Firebase, você deve receber uma mensagem como a mostrada abaixo:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Verifique se o projeto está listado em [!DNL Firebase ]console](https://console.firebase.google.com/)

## Configurar [!UICONTROL Push Channel] Configurações

1. Fazer logon em [!DNL Firebase] console
2. Abra o **[!UICONTROL ACSPushTutorial]** projeto.
3. Clique em **ícone de engrenagem** e abra as configurações do projeto

   ![configurações-projeto](assets/firebase-project-settings.PNG)

4. Guia para a **[!UICONTROL Cloud Messaging]** guia.
5. Copiar a chave do servidor

   ![server-key](assets/firebase-server-key.PNG)

6. Faça logon na sua instância do Adobe Campaign Standard
7. Clique em **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selecione o apropriado **[!UICONTROL Mobile Application Property].**
9. Clique em **[!DNL Android]ícone** no **[!UICONTROL Push Channel settings]** seção.
10. Cole a chave do servidor no campo de chave do servidor.

Se tudo correr bem, você verá uma mensagem de SUCESSO.

![push-channel-settings](assets/push-channel-settings.PNG)

Em resumo, criamos uma [!DNL Android App] e conectou o [!DNL Android App] com [!DNL Firebase]. Em seguida, conectamos o aplicativo móvel no Adobe Campaign com o [!DNL Android App] colando o [!DNL Android] Chave do servidor do aplicativo no Aplicativo móvel no Adobe Campaign Standard.
