---
title: Configurar eventos
description: 'Ao configurar uma mensagem no aplicativo nos eventos Adobe Campaign Standard (ACS), defina qual ação iniciada pelo usuário disparará a mensagem a ser exibida. '
feature: In-App
topics: Mobile
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 11263e247184ddc6a8e3df6a8ed0899907fbb366
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 3%

---


# Configurar [!UICONTROL Events] {#configuring-events}

Ao configurar uma mensagem [!UICONTROL In-App], é necessário definir qual ação iniciada pelo usuário aciona a mensagem a ser exibida. Essas ações são chamadas de [!UICONTROL events]. Três categorias de [!UICONTROL events] estão disponíveis: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events] e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] são  [!UICONTROL custom events] implementados em seu aplicativo móvel.

Os exemplos são:

* Um cliente visualizou um item
* Um cliente adiciona um item ao carrinho
* Abandono de carrinho
* Um cliente comprou algo

Você deve configurar esses [!UICONTROL events] no Adobe Campaign. O vídeo a seguir descreve como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] estão prontos para uso  [!UICONTROL events]. Os seguintes [!UICONTROL events] estão disponíveis:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Um exemplo de caso de uso pode ser uma mensagem que apresenta novos recursos após uma atualização ou uma promoção de evento.

>[!NOTE]
>
>O [!UICONTROL Lifecycle module] precisa ser configurado no aplicativo móvel. Consulte aqui para obter mais informações sobre [Como adicionar o Lifecycle ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

As três categorias a seguir são suportadas, dependendo do instrumentado no aplicativo móvel:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] exigir uma licença da Adobe Analytics. Depois que você tiver a extensão [[!DNL Analytics] configurada](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e tiver adicionado [o Analytics ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), esses eventos ficarão disponíveis na configuração [!UICONTROL In-App] no ACS.

## Recursos adicionais

* [Ativar Medições de Ciclo de Vida (documentação)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
