---
title: Configurar eventos
description: "Entenda como os eventos definem qual ação iniciada pelo usuário acionará a exibição de uma mensagem no aplicativo. "
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 89df23d00913d36b93d3be03b62c74320524f9c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# Configurar [!UICONTROL Events] {#configuring-events}

Ao configurar um [!UICONTROL In-App] você precisa definir qual ação iniciada pelo usuário aciona a mensagem a ser exibida. Essas ações são chamadas de [!UICONTROL events]. Três categorias [!UICONTROL events] estão disponíveis: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events], e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] são [!UICONTROL custom events] que são implementadas no aplicativo móvel.

São exemplos:

* Um cliente visualizou um item
* Um cliente adiciona um item ao carrinho
* Abandono do carrinho
* Um cliente comprou algo

Você deve configurar estes [!UICONTROL events] no Adobe Campaign. O vídeo a seguir descreve como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] são prontos para uso [!UICONTROL events]. As seguintes [!UICONTROL events] estão disponíveis:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Um exemplo de caso de uso pode ser uma mensagem apresentando novos recursos após uma atualização ou uma promoção de evento.

>[!NOTE]
>
>A variável [!UICONTROL Lifecycle module] precisa ser configurado no aplicativo móvel. Clique aqui para obter mais informações sobre [Como adicionar um ciclo de vida ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

As três categorias a seguir têm suporte, dependendo do que é instrumentado no aplicativo móvel:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] exigir uma licença do Adobe Analytics. Depois que você tiver o [[!DNL Analytics] extensão configurada](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e adicionaram [Analytics para o seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), esses eventos ficarão disponíveis no [!UICONTROL In-App] no ACS.
