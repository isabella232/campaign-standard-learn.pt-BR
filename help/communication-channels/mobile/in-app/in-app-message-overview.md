---
title: Introdução às mensagens no aplicativo
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
ht-degree: 19%

---


# Introdução às [!UICONTROL In-App] mensagens {#introduction}

O [!UICONTROL In-App Messaging] canal permite exibir uma mensagem quando o usuário está ativo no aplicativo móvel. Este canal exige a integração de aplicativos móveis com [!UICONTROL Adobe Experience Platform SDK].

Este tutorial explicará as etapas necessárias para configurar as propriedades móveis, a [!UICONTROL Launch] extensão do [!UICONTROL In-App Messaging] canal, bem como como como preparar, personalizar e enviar [!UICONTROL In-App] mensagens no Adobe Campaign Standard. Os links o levarão aos tutoriais em vídeo de cada um dos tópicos destacados.

## Pré-requisitos {#prerequisites}

1. Verifique se você pode acessar o **[!UICONTROL In-App]** canal. Se não conseguir acessar esses canais, entre em contato com sua equipe de conta.
1. Verify that your **user** has the necessary **permissions** in Adobe Campaign Standard and [!UICONTROL Launch].

   1. No Adobe Campaign Standard, verifique se o usuário do IMS faz parte dos grupos [!UICONTROL Standard User] e [!UICONTROL Administrator] .\
      Essa etapa permite que o usuário faça logon no Adobe Campaign Standard, navegue até a página do aplicativo móvel SDK do Experience Platform e visualização as propriedades do aplicativo móvel que você criou no [!UICONTROL Launch].
   1. Em [!UICONTROL Launch], verifique se o usuário do IMS faz parte de um perfil de [!UICONTROL Launch] produto.\
      Essa etapa permite que o usuário faça logon para [!UICONTROL Launch] criar e visualização as propriedades. Para obter mais informações sobre perfis de produtos em [!UICONTROL Launch], consulte [Criar perfil](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile)de produtos. No perfil do produto, não deve haver permissões definidas na empresa ou nas propriedades, mas o usuário ainda pode fazer logon.

1. No Adobe Experience Platform Launch:

   1. Crie o aplicativo móvel criando uma propriedade móvel e instrua seu aplicativo móvel com SDK Experience Platform.
   1. Instale a extensão do **Adobe Campaign Standard** para seu aplicativo móvel.

Para obter mais informações sobre extensões, consulte a extensão [Configurar Campaign Standard no Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) na [!UICONTROL Adobe Launch ]documentação.

## Etapas para configurar [!UICONTROL In-App] mensagens {#steps-to-set-up}

1. [Configure um aplicativo móvel usando o Adobe Experience Platform SDK](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [Configure eventos](/help/communication-channels/mobile/in-app/configure-events.md).

## Criar, gerenciar e publicar [!UICONTROL In-App] Delivery {#create-manage-publish}

Você pode criar delivery no aplicativo uma vez clicando no **[!UICONTROL Create an In-App Message]** cartão na página inicial, na página [!UICONTROL Marketing Activities]inicial ou pode [Criar um delivery no aplicativo em um fluxo de trabalho](/help/communication-channels/mobile/in-app/in-app-activity.md).

Ao configurar o delivery, você tem três opções para público alvo de seus usuários escolhendo entre diferentes templates do delivery:

1. [**Transmita uma mensagem **](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md)no aplicativo para público alvo de todos os usuários de um aplicativo móvel.

   esse tipo de mensagem permite enviar mensagens para todos os usuários (atuais ou futuros) do seu aplicativo móvel, mesmo que eles não tenham um perfil existente no Adobe Campaign. Portanto, a personalização não é possível ao personalizar as mensagens, pois o perfil do usuário não existe necessariamente no Adobe Campaign.

1. Público alvo todos os usuários com base no perfil do aplicativo móvel.

   esse tipo de mensagem permite direcionar todos os usuários conhecidos ou anônimos de um aplicativo móvel que tenha um perfil móvel no Adobe Campaign. Esse tipo de mensagem pode ser personalizado usando apenas atributos não pessoais e não confidenciais e não requer handshake seguro entre o Mobile SDK e o serviço de mensagens no aplicativo do Adobe Campaign. Então, a estratégia de personalização é baseada no que você aprendeu sobre os usuários da interação deles com o dispositivo. Por exemplo, público alvo todos os usuários que inicializaram seu aplicativo mais de cinco vezes na última semana.

1. [**Usuários do Público alvo com base em seus perfis **](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md)de Campanha.

   esse tipo de mensagem permite direcionar perfis do Adobe Campaign (perfis CRM) que assinaram seu aplicativo para dispositivos móveis. A mensagem pode ser personalizada com todos os atributos de perfil disponíveis no Adobe Campaign, mas requer um handshake seguro entre o SDK móvel e o serviço de mensagens no aplicativo Campaign para garantir que as mensagens com informações pessoais e confidenciais sejam usadas apenas por usuários autorizados.

Este modelo é útil para suportar casos de uso de orquestração entre canais, nos quais você já direcionou usuários para outros canais, como Email ou Push, e com base em sua resposta, você deseja engajá-los com uma mensagem no aplicativo.

## Relatório sobre seus delivery no aplicativo {#report}

Depois que seu delivery for publicado, você poderá [gerar relatórios sobre seu delivery](/help/communication-channels/mobile/in-app/in-app-reporting.md)no aplicativo.

## Recursos adicionais

* [Relatório no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Configurar uma propriedade móvel](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Configurar um aplicativo móvel usando SDKs do Adobe Experience Platform](https://helpx.adobe.com/br/campaign/kb/configuring-app-sdk.html)
* [Preparação e envio de uma mensagem no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Personalização de mensagem no aplicativo](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Envio de uma mensagem no aplicativo em um workflow](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Ativar Medições de Ciclo de Vida](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
