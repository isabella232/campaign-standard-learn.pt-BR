---
title: Noções básicas sobre o conector de dados do Adobe Experience Platform
description: O Adobe Experience Platform Data Connector ajuda os clientes existentes a disponibilizar seus dados no Adobe Experience Platform, mapeando dados XTK (dados assimilados no Campaign) para dados do Experience Data Model (XDM) no Adobe Experience Platform.
feature: People Core Service Integration
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 2ba22e7e7d193278fd06cb4b2dc80f650f754ec8
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---

# Entender a Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esse recurso está em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>Entre em contato com o [!UICONTROL Adobe Customer Support] se você planeja implementar esse recurso.

## Visão geral

Adobe Experience Platform [!UICONTROL Data Connector] ajuda os clientes existentes a disponibilizarem seus dados no Adobe Experience Platform, mapeando os dados XTK (dados assimilados no Adobe Campaign) para [!DNL Experience Data Model] (XDM) no Adobe Experience Platform.

O conector é unidirecional e envia os dados do Adobe Campaign Standard para o Adobe Experience Platform. Os dados nunca são enviados da Adobe Experience Platform para a Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] destina-se a engenheiros de dados que compreendem a Adobe Campaign Standard [!UICONTROL custom resources] e ter uma compreensão de como o schema de dados geral do cliente deve estar dentro do Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Este vídeo fornece uma visão geral sobre a Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>A transferência pronta para uso do [!UICONTROL subscription events] não é suportado. Para transferência [!UICONTROL subscription events], você pode criar XDM e conjunto de dados correspondentes no Adobe Experience Platform e, em seguida, configurar um mapeamento de dados personalizado para esses dados.
>
>Existente [!UICONTROL experience events] não pode ser assimilado no Adobe Experience Platform, mas gerado continuamente [!UICONTROL experience events] são transmitidos para o Adobe Experience Platform.

## Etapas principais para executar um mapeamento de dados

Os seguintes tutoriais descrevem as principais etapas para executar um mapeamento de dados entre o Campaign Standard e o Adobe Experience Platform:

1. [Mapeamento de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapeamento de eventos de experiência](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mapeamento de dados da tabela de propagação](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificação do mapeamento de dados](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificar o status dos trabalhos de assimilação de dados](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Recursos adicionais

* [Sobre o Conector de dados da Adobe Experience Platform](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-about-data-connector.html)

