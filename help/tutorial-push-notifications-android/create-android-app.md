---
title: Etapa 1 - Criação de aplicativos Android e configuração para usar o Firebase Cloud Messaging
description: Nesta parte, criaremos [!DNL Android] App to receive [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Para receber as notificações por push, o aplicativo precisa ser registrado com o  [!DNL Firebase Cloud Service] do Google.
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Etapa 1 - Criação do aplicativo [!DNL Android] e configuração para usar [!DNL Firebase Cloud Messaging]

Nesta parte, você criará [!DNL Android] aplicativo para receber [!UICONTROL Push notifications] enviado do Adobe Campaign Standard. Para receber as notificações por push, o aplicativo precisa ser registrado no [!DNL Firebase Cloud Service] do Google.

1. Faça logon em sua conta [!DNL Firebase].

   [!DNL Firebase] A é a plataforma móvel do Google que ajuda você a desenvolver rapidamente aplicativos de alta qualidade. Se você não tiver uma conta [!DNL Firebase], crie um [daqui](https://firebase.google.com).

2. Iniciar [!DNL Android Studio]
3. Clique em **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Selecione **[!UICONTROL Empty Activity]** e clique em **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Forneça um nome significativo para o projeto.

   Para o objetivo desta demonstração, nomeamos nosso projeto como *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Aceite os nomes de pacote padrão e clique em **[!DNL Finish]** para criar o projeto.
7. A estrutura do projeto deve ser semelhante à captura de tela abaixo

   ![android-project-structure](assets/android-project-structure.PNG)

8. Clique em **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (isso adiciona o projeto ao  [!DNL Firebase])
9. Clique em **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![configurar o firebase](assets/android-project-firebase-messaging.PNG)

10. Clique em **[!UICONTROL Connect to Firebase].**
11. Depois que seu aplicativo estiver conectado ao Firebase, clique em **[!UICONTROL Add FCM to your app].**
12. Clique em **[!UICONTROL Accept Changes].**

   Ao adicionar o FCM ao aplicativo, o assistente precisa da permissão para fazer algumas alterações no projeto.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

Na integração bem-sucedida do seu aplicativo com o Firebase, você deve receber uma mensagem como a mostrada abaixo:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Certifique-se de que o projeto esteja listado  [!DNL Firebase ]no console](https://console.firebase.google.com/)

## Definir configurações [!UICONTROL Push Channel]

1. Faça logon no console [!DNL Firebase]
2. Abra o projeto **[!UICONTROL ACSPushTutorial]**.
3. Clique no **ícone de engrenagem** e abra as configurações do projeto

   ![configurações do projeto](assets/firebase-project-settings.PNG)

4. Toque na guia **[!UICONTROL Cloud Messaging]** .
5. Copiar a chave do servidor

   ![chave do servidor](assets/firebase-server-key.PNG)

6. Faça logon na sua instância do Adobe Campaign Standard
7. Clique em **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Selecione o **[!UICONTROL Mobile Application Property]apropriado.**
9. Clique no ícone **[!DNL Android]** na seção **[!UICONTROL Push Channel settings]**.
10. Cole a chave do servidor no campo Server key .

Se tudo correr bem, você deverá ver uma mensagem de SUCESSO.

![configurações de canal de push](assets/push-channel-settings.PNG)

Para resumir, criamos um [!DNL Android App] e conectamos o [!DNL Android App] com [!DNL Firebase]. Em seguida, conectamos o Aplicativo móvel no Adobe Campaign com o [!DNL Android App] colando a chave do servidor do [!DNL Android] no Aplicativo móvel no Adobe Campaign Standard.
