---
title: Etapa 1 - Criação de aplicativos Android e configuração para usar o Firebase Cloud Messaging
description: Nesta parte, criaremos [!DNL Android] App to receive [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Para receber notificações por push, o aplicativo precisa ser registrado no Google [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# Etapa 1 - Criação [!DNL Android] Aplicativo e configuração para usar [!DNL Firebase Cloud Messaging]

Nesta parte, você criará [!DNL Android] Aplicativo para recebimento [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Para receber notificações por push, o aplicativo precisa ser registrado no Google [!DNL Firebase Cloud Service].

1. Faça logon no [!DNL Firebase] conta.

   [!DNL Firebase] A é a plataforma móvel Google que ajuda você a desenvolver rapidamente aplicativos de alta qualidade. Se você não tiver um [!DNL Firebase] criar uma conta [daqui](https://firebase.google.com).

2. Launch [!DNL Android Studio]
3. Clique em **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selecione **[!UICONTROL Empty Activity]** e clique em **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Forneça um nome significativo para o projeto.

   Para o objetivo desta demonstração, nomeamos o nosso projeto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Aceite os nomes de pacote padrão e clique em **[!DNL Finish]** para criar o projeto.
7. A estrutura do projeto deve ser semelhante à captura de tela abaixo

   ![android-project-structure](assets/android-project-structure.PNG)

8. Clique em **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (isso adiciona o projeto ao [!DNL Firebase])
9. Clique em **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar o firebase](assets/android-project-firebase-messaging.PNG)

10. Clique em **[!UICONTROL Connect to Firebase].**
11. Depois que seu aplicativo estiver conectado ao Firebase, clique em **[!UICONTROL Add FCM to your app].**
12. Clique em **[!UICONTROL Accept Changes].**

   Ao adicionar o FCM ao aplicativo, o assistente precisa da permissão para fazer algumas alterações no projeto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Na integração bem-sucedida do seu aplicativo com o Firebase, você deve receber uma mensagem como a mostrada abaixo:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Certifique-se de que o projeto esteja listado em [!DNL Firebase ]console](https://console.firebase.google.com/)

## Configurar [!UICONTROL Push Channel] Configurações

1. Faça logon em [!DNL Firebase] console
2. Abra o **[!UICONTROL ACSPushTutorial]** projeto.
3. Clique no botão **ícone de engrenagem** e abra as configurações do projeto

   ![configurações do projeto](assets/firebase-project-settings.PNG)

4. Guia para **[!UICONTROL Cloud Messaging]** guia .
5. Copiar a chave do servidor

   ![chave do servidor](assets/firebase-server-key.PNG)

6. Faça logon na sua instância do Adobe Campaign Standard
7. Clique em **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selecione o **[!UICONTROL Mobile Application Property].**
9. Clique no botão **[!DNL Android]ícone** no **[!UICONTROL Push Channel settings]** seção.
10. Cole a chave do servidor no campo Server key .

Se tudo correr bem, você deverá ver uma mensagem de SUCESSO.

![configurações de canal de push](assets/push-channel-settings.PNG)

Para resumir, criamos um [!DNL Android App] e conectada a [!DNL Android App] com [!DNL Firebase]. Em seguida, conectamos o aplicativo móvel no Adobe Campaign com a [!DNL Android App] colando o [!DNL Android] Chave do servidor do aplicativo no Aplicativo móvel do Adobe Campaign Standard.
