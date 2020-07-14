---
title: Configurar Eventos
description: 'Ao configurar uma mensagem no aplicativo em eventos Adobe Campaign Standard (ACS), defina qual ação iniciada pelo usuário disparará a mensagem a ser exibida. '
feature: In-App
topics: Mobile
kt: 2548
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Configurar [!UICONTROL Events] {#configuring-events}

Ao configurar uma [!UICONTROL In-App] mensagem, é necessário definir qual ação iniciada pelo usuário aciona a mensagem a ser exibida. Essas ações são chamadas [!UICONTROL events]. Três categorias de [!UICONTROL events] estão disponíveis: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]e [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] são [!UICONTROL custom events] implementados em seu aplicativo móvel.

Os exemplos são:

* Um cliente visualizou um item
* Um cliente adiciona um item ao carrinho
* Abandono de carrinho
* Um cliente comprou algo

Você deve configurá-los [!UICONTROL events] no Adobe Campaign. O vídeo a seguir descreve como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] estão prontos para uso [!UICONTROL events]. The following [!UICONTROL events] are available:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Um exemplo de caso de uso pode ser uma mensagem que apresenta novos recursos após uma atualização ou uma promoção de evento.

>[!NOTE]
>
>O aplicativo móvel [!UICONTROL Lifecycle module] precisa ser configurado. Consulte aqui para obter mais informações sobre [como adicionar o ciclo de vida ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

As três categorias a seguir são suportadas, dependendo do instrumentado no aplicativo móvel:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] exigir uma licença da Adobe Analytics. Depois que você tiver a [[!DNL Analytics] extensão configurada](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) e tiver adicionado o [Analytics ao seu aplicativo](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), esses eventos ficarão disponíveis na configuração do [!UICONTROL In-App] ACS.

## Recursos adicionais

* [Ativar Medições de Ciclo de Vida (documentação)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
