---
title: Noções básicas sobre o conector de dados Adobe Experience Platform
description: O Adobe Experience Platform Data Connector ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando os dados XTK (dados ingeridos na Campanha) para os dados do Experience Data Model (XDM) no Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 5%

---


# Como entender o Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esse recurso está atualmente em beta e sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>Entre em contato se [!UICONTROL Adobe Customer Support] planeja implementar esse recurso.

## Visão geral

O Adobe Experience Platform [!UICONTROL Data Connector] ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando os dados XTK (dados ingeridos no Adobe Campaign) para [!DNL Experience Data Model] (XDM) no Adobe Experience Platform.

Observe que o conector é unidirecional e envia os dados de Adobe Campaign Standard para Adobe Experience Platform. Os dados nunca são enviados do Adobe Experience Platform para o Adobe Campaign Standard.

O Adobe Experience Platform [!UICONTROL Data Connector] destina-se aos engenheiros de dados que entendem a Adobe Campaign Standard [!UICONTROL custom resources] e que têm uma ideia de como o schema geral de dados do cliente deve estar dentro da Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo fornece uma visão geral sobre o Adobe Experience Platform[!UICONTROL Data Connector](09:35 min)*

>[!NOTE]
>
>A transferência predefinida de [!UICONTROL subscription events] não é suportada. Para transferir [!UICONTROL subscription events], você pode criar XDM e conjunto de dados correspondentes no Adobe Experience Platform e, em seguida, configurar um mapeamento de dados personalizado para esses dados.
>
>Não é [!UICONTROL experience events] possível ingerir o existente no Adobe Experience Platform, mas a geração contínua [!UICONTROL experience events] será transmitida para o Adobe Experience Platform.

## Etapas principais para executar um mapeamento de dados

Os seguintes tutoriais descrevem as etapas principais para executar um mapeamento de dados entre Campaign Standard e Adobe Experience Platform:

1. [Mapeamento de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapeamento de Eventos de experiência](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mapeamento de dados da tabela de sementes](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificação do mapeamento de dados](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificando o status de trabalhos de ingestão de dados](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionais

* [Sobre o Conector de dados da Adobe Experience Platform](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Visão geral do Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definição de mapeamento](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Ativação de mapeamento](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Acionando a assimilação de dados por meio de APIs](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
