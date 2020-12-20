---
title: Introdução a mensagens no aplicativo
description: O canal de mensagens no aplicativo (ACS) da Adobe Campaign Standard permite que você apresente ao usuário mensagens no aplicativo contextualmente relevantes em resposta ao comportamento em tempo real do cliente no aplicativo móvel.
feature: In-App
topics: Mobile
kt: 1911
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 20%

---


# Introdução às mensagens [!UICONTROL In-App] {#introduction}

O canal [!UICONTROL In-App Messaging] permite exibir uma mensagem quando o usuário está ativo no aplicativo móvel. Este canal exige que os aplicativos móveis sejam integrados com [!UICONTROL Adobe Experience Platform SDK].

Este tutorial explicará as etapas necessárias para configurar as propriedades móveis, a extensão [!UICONTROL Launch] para o canal [!UICONTROL In-App Messaging], bem como como preparar, personalizar e enviar mensagens [!UICONTROL In-App] no Adobe Campaign Standard. Os links o levarão aos tutoriais em vídeo de cada um dos tópicos destacados.

## Pré-requisitos {#prerequisites}

1. Verifique se você pode acessar o canal **[!UICONTROL In-App]**. Se não conseguir acessar esses canais, entre em contato com sua equipe de conta.
1. Verifique se seu **usuário** tem as **permissões** necessárias no Adobe Campaign Standard e [!UICONTROL Launch].

   1. No Adobe Campaign Standard, verifique se o usuário IMS faz parte dos grupos [!UICONTROL Standard User] e [!UICONTROL Administrator].\
      Esta etapa permite que o usuário faça logon no Adobe Campaign Standard, navegue até a página do aplicativo móvel Experience Platform SDK e visualização as propriedades do aplicativo móvel que você criou em [!UICONTROL Launch].
   1. Em [!UICONTROL Launch], certifique-se de que seu usuário IMS faça parte de um perfil de produto [!UICONTROL Launch].\
      Esta etapa permite que o usuário faça logon em [!UICONTROL Launch] para criar e visualização as propriedades. Para obter mais informações sobre perfis de produtos em [!UICONTROL Launch], consulte [Criar perfil de produto](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile). No perfil do produto, não deve haver permissões definidas na empresa ou nas propriedades, mas o usuário ainda pode fazer logon.

1. No Adobe Experience Platform Launch:

   1. Crie o aplicativo móvel criando uma propriedade móvel e instrua seu aplicativo móvel com SDK Experience Platform.
   1. Instale a extensão **Adobe Campaign Standard** para seu aplicativo móvel.

Para obter mais informações sobre extensões, consulte a extensão [Configure Campaign Standard em Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) na documentação [!UICONTROL Adobe Launch ].

## Etapas para configurar [!UICONTROL In-App] mensagens {#steps-to-set-up}

1. [Configure um aplicativo móvel usando o Adobe Experience Platform SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [Configure eventos](/help/communication-channels/mobile/in-app/configure-events.md).

## Criar, gerenciar e publicar Delivery [!UICONTROL In-App] {#create-manage-publish}

Você pode criar delivery no aplicativo uma vez clicando no cartão **[!UICONTROL Create an In-App Message]** da página inicial, de [!UICONTROL Marketing Activities], ou pode [Criar um delivery no aplicativo em um fluxo de trabalho](/help/communication-channels/mobile/in-app/in-app-activity.md).

Ao configurar o delivery, você tem três opções para público alvo de seus usuários escolhendo entre diferentes templates do delivery:

1. [**Transmita uma**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) mensagem no aplicativo para público alvo de todos os usuários de um aplicativo móvel.

   esse tipo de mensagem permite enviar mensagens para todos os usuários (atuais ou futuros) do seu aplicativo móvel, mesmo que eles não tenham um perfil existente no Adobe Campaign. Portanto, a personalização não é possível ao personalizar as mensagens, pois o perfil do usuário não existe necessariamente no Adobe Campaign.

1. Público alvo todos os usuários com base no perfil do aplicativo móvel.

   esse tipo de mensagem permite direcionar todos os usuários conhecidos ou anônimos de um aplicativo móvel que tenha um perfil móvel no Adobe Campaign. Esse tipo de mensagem pode ser personalizado usando apenas atributos não pessoais e não confidenciais e não requer handshake seguro entre o Mobile SDK e o serviço de mensagens no aplicativo do Adobe Campaign. Então, a estratégia de personalização é baseada no que você aprendeu sobre os usuários da interação deles com o dispositivo. Por exemplo, público alvo todos os usuários que inicializaram seu aplicativo mais de cinco vezes na última semana.

1. [**Direcionar usuários com base em seus perfis do Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   esse tipo de mensagem permite direcionar perfis do Adobe Campaign (perfis CRM) que assinaram seu aplicativo para dispositivos móveis. A mensagem pode ser personalizada com todos os atributos de perfil disponíveis no Adobe Campaign, mas requer um handshake seguro entre o SDK móvel e o serviço de mensagens no aplicativo Campaign para garantir que as mensagens com informações pessoais e confidenciais sejam usadas apenas por usuários autorizados.

Este modelo é útil para suportar casos de uso de orquestração entre canais, nos quais você já direcionou usuários para outros canais, como Email ou Push, e com base em sua resposta, você deseja engajá-los com uma mensagem no aplicativo.

## Relatório sobre seus delivery no aplicativo {#report}

Depois que seu delivery for publicado, você poderá [relatar seu delivery no aplicativo](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## Recursos adicionais

* [Relatório no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Configurar uma propriedade móvel](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configurar um aplicativo móvel usando SDKs do Adobe Experience Platform](https://helpx.adobe.com/br/campaign/kb/configuring-app-sdk.html)
* [Preparação e envio de uma mensagem no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personalização de mensagem no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Envio de uma mensagem no aplicativo em um workflow](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Ativar Medições de Ciclo de Vida](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
