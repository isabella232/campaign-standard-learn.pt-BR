---
title: Configurar eventos
description: '"Entenda como os eventos definem qual ação iniciada pelo usuário acionará uma mensagem no aplicativo a ser exibida. "'
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# Configurar [!UICONTROL Events] {#configuring-events}

Ao configurar um [!UICONTROL In-App] , é necessário definir qual ação iniciada pelo usuário aciona a mensagem a ser exibida. Essas ações são chamadas de [!UICONTROL events]. Três categorias de [!UICONTROL events] estão disponíveis: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] são [!UICONTROL custom events] que são implementadas no aplicativo móvel.

Os exemplos são:

* Um cliente visualizou um item
* Um cliente adiciona um item ao carrinho
* Abandono do carrinho
* Um cliente comprou algo

Você deve configurá-los [!UICONTROL events] no Adobe Campaign. O vídeo a seguir descreve como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] são prontas para uso [!UICONTROL events]. O seguinte [!UICONTROL events] estão disponíveis:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Um exemplo de caso de uso pode ser uma mensagem que apresenta novos recursos após uma atualização ou uma promoção de evento.

>[!NOTE]
>
>O [!UICONTROL Lifecycle module] precisa ser configurado no aplicativo móvel. Consulte aqui para obter mais informações sobre [Como adicionar o Lifecycle ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

As três categorias a seguir são suportadas, dependendo do que é instrumentado no aplicativo móvel:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] exige uma licença da Adobe Analytics. Assim que tiver o [[!DNL Analytics] extensão configurada](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e [Analytics para seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), esses eventos ficam disponíveis na variável [!UICONTROL In-App] no ACS.

## Recursos adicionais

* [Ativar Medições de ciclo de vida (documentação)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
