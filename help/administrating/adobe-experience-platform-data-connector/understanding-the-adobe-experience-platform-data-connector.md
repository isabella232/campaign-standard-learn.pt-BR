---
title: Entender o conector de dados do Adobe Experience Platform
description: O Conector de dados do Adobe Experience Platform ajuda os clientes existentes a disponibilizar seus dados no Adobe Experience Platform, mapeando os dados XTK (dados assimilados no Campaign) para dados do Experience Data Model (XDM) no Adobe Experience Platform.
feature: People Core Service Integration
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 89df23d00913d36b93d3be03b62c74320524f9c7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 4%

---

# Entender a Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Esse recurso está na versão beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>Entre em contato com [!UICONTROL Adobe Customer Support] se você planeja implementar esse recurso.

## Visão geral

Adobe Experience Platform [!UICONTROL Data Connector] O ajuda os clientes existentes a disponibilizar seus dados no Adobe Experience Platform, mapeando os dados XTK (dados assimilados no Adobe Campaign) para [!DNL Experience Data Model] (XDM) no Adobe Experience Platform.

O conector é unidirecional e envia os dados do Adobe Campaign Standard para a Adobe Experience Platform. Os dados nunca são enviados da Adobe Experience Platform para o Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] O é destinado aos engenheiros de dados que compreendem o Adobe Campaign Standard [!UICONTROL custom resources] e entender como o esquema de dados geral do cliente deve estar dentro da Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12&learn=on)

*Este vídeo fornece uma visão geral sobre o Adobe Experience Platform [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>A transferência pronta para uso de [!UICONTROL subscription events] não é compatível. Para transferir [!UICONTROL subscription events], você pode criar o XDM e o conjunto de dados correspondentes no Adobe Experience Platform e, em seguida, configurar um mapeamento de dados personalizado para esses dados.
>
>Existente [!UICONTROL experience events] não pode ser assimilado na Adobe Experience Platform, mas gerado continuamente [!UICONTROL experience events] são transmitidos para o Adobe Experience Platform.

## Etapas principais para executar um mapeamento de dados

Os tutoriais a seguir descrevem as principais etapas para executar um mapeamento de dados entre o Campaign Standard e o Adobe Experience Platform:

1. [Mapeamento de recursos personalizados](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapeamento de eventos de experiência](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mapeamento de dados da tabela de seed](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Modificação do Mapeamento de Dados](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Verificar o status dos trabalhos de assimilação de dados](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

