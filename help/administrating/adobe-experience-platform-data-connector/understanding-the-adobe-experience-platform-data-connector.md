---
title: Saiba mais sobre o Conector de dados da Adobe Experience Platform
description: O Adobe Experience Platform Data Connector ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando dados XTK (dados ingeridos na Campanha) para dados do Experience Data Model (XDM) no Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: d87971b70bde8de1822f18cbafd8e2d7b4808edc
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 10%

---


# Como entender o Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esse recurso está atualmente em beta e sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>Entre em contato se [!UICONTROL Adobe Customer Support] planeja implementar esse recurso.

## Visão geral

A Adobe Experience Platform [!UICONTROL Data Connector] ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando dados XTK (dados ingeridos no Adobe Campaign) para [!DNL Experience Data Model] (XDM) no Adobe Experience Platform.

Observe que o conector é unidirecional e envia os dados da Adobe Campaign Standard para a Adobe Experience Platform. Os dados nunca são enviados da Adobe Experience Platform para a Adobe Campaign Standard.

A Adobe Experience Platform [!UICONTROL Data Connector] destina-se aos engenheiros de dados que entendem a Adobe Campaign Standard [!UICONTROL custom resources] e têm uma ideia de como o schema geral de dados do cliente deve estar dentro da Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo oferece uma visão geral sobre o Adobe Experience Platform[!UICONTROL Data Connector](9:35 min)*

>[!NOTE]
>
>A transferência predefinida de [!UICONTROL subscription events] não é suportada. Para transferir [!UICONTROL subscription events], você pode criar XDM e conjunto de dados correspondentes no Adobe Experience Platform e, em seguida, configurar um mapeamento de dados personalizado para esses dados.
>
>O existente [!UICONTROL experience events] não pode ser ingerido no Adobe Experience Platform, mas o gerado em andamento [!UICONTROL experience events] será transmitido ao Adobe Experience Platform.

## Etapas principais para executar um mapeamento de dados

Os seguintes tutoriais descrevem as etapas principais para executar um mapeamento de dados entre o Campaign Standard e o Adobe Experience Platform:

1. [Mapeamento de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapeamento de eventos de experiência](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mapeamento de dados da tabela de sementes](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificação do mapeamento de dados](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificar status dos trabalhos de assimilação de dados](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionais

* [Sobre o Conector de dados da Adobe Experience Platform](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Visão geral do Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definição de mapeamento](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Ativação de mapeamento](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Acionando a assimilação de dados por meio de APIs](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
