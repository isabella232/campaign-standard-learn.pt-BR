---
title: Saiba mais sobre o Conector de dados da Adobe Experience Platform
description: O Adobe Experience Platform Data Connector ajuda os clientes existentes a disponibilizar seus dados no Adobe Experience Platform, mapeando dados XTK (dados assimilados no Campaign) para dados do Experience Data Model (XDM) no Adobe Experience Platform.
feature: Integração do Serviço principal de pessoas
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 64940a739897c3969574dcf1d1e36c5a986d0473
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 10%

---

# Entendendo o Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>No momento, esse recurso está em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>Entre em contato com [!UICONTROL Adobe Customer Support] se planeja implementar esse recurso.

## Visão geral

O Adobe Experience Platform [!UICONTROL Data Connector] ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando dados XTK (dados assimilados no Adobe Campaign) para [!DNL Experience Data Model] (XDM) dados no Adobe Experience Platform.

Observe que o conector é unidirecional e envia os dados do Adobe Campaign Standard para o Adobe Experience Platform. Os dados nunca são enviados da Adobe Experience Platform para a Adobe Campaign Standard.

O Adobe Experience Platform [!UICONTROL Data Connector] é destinado a engenheiros de dados que compreendem o Adobe Campaign Standard [!UICONTROL custom resources] e que compreendem como o esquema de dados geral do cliente deve estar dentro do Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo fornece uma visão geral sobre a Adobe Experience Platform  [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>A transferência predefinida de [!UICONTROL subscription events] não é suportada. Para transferir [!UICONTROL subscription events], você pode criar XDM e conjunto de dados correspondentes no Adobe Experience Platform e, em seguida, configurar um mapeamento de dados personalizado para esses dados.
>
>[!UICONTROL experience events] existente não pode ser assimilado no Adobe Experience Platform, mas o [!UICONTROL experience events] gerado continuamente será transmitido para o Adobe Experience Platform.

## Etapas principais para executar um mapeamento de dados

Os seguintes tutoriais descrevem as principais etapas para executar um mapeamento de dados entre o Campaign Standard e o Adobe Experience Platform:

1. [Mapeamento de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapeamento de eventos de experiência](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mapeamento de dados da tabela de propagação](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificação do mapeamento de dados](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificação do status dos trabalhos de assimilação de dados](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionais

* [Sobre o Conector de dados da Adobe Experience Platform](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Visão geral do Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Definição de mapeamento](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-mapping-definition.html)
* [Ativação de mapeamento](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-mapping-activation.html)
* [Acionando a assimilação de dados por meio de APIs](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-triggering-data-ingestion.html)
