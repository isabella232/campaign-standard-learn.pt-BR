---
title: Atividade de sinal externo - Chame um fluxo de trabalho com parâmetros
description: A Atividade de sinal externo é usada para organizar e orquestrar diferentes processos que fazem parte da mesma jornada do cliente para workflows diferentes. Ele permite start de um fluxo de trabalho de outro, permitindo suportar jornadas de clientes mais complexas, ao mesmo tempo que pode monitorar e reagir melhor em caso de problema.
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: b95fb2360d6336c941e7b92a6e2abb376185a7c3
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# [!UICONTROL External Signal activity ]- Chamar um fluxo de trabalho com parâmetros

O [!UICONTROL External Signal activity] é usado para organizar e orquestrar diferentes processos que fazem parte da mesma jornada do cliente para workflows diferentes. Ele permite start de um fluxo de trabalho de outro, permitindo suportar jornadas de clientes mais complexas, ao mesmo tempo que pode monitorar e reagir melhor em caso de problema.

No ACS 19.2, o [!UICONTROL External Signal activity] pode não apenas chamar um fluxo de trabalho, mas também enviar parâmetros para o fluxo de trabalho (um nome de audiência para o público alvo, um nome de arquivo a ser importado, uma parte do conteúdo da mensagem etc.) para o fluxo de trabalho a partir de outro fluxo de trabalho ou chamada REST API para integração com seus sistemas externos.

Isso também inclui uma nova Atividade **de teste** , na qual você pode executar testes sobre essa funcionalidade.

O vídeo a seguir explica as etapas de configuração necessárias para:

1. **Receba parâmetros** externos de um sistema externo, como um sistema de gestão de conteúdo (CRM):

   * Declarar os parâmetros na Atividade de sinal externo
   * Configure a chamada da API para definir os parâmetros e disparar a Atividade do sinal externo do fluxo de trabalho. Para obter mais informações sobre como configurar uma chamada de API, consulte [Acionando uma Atividade](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity)de sinal.

1. **Personalize um fluxo de trabalho com parâmetros** externos (variáveis de eventos):

   Depois que o fluxo de trabalho é acionado, os parâmetros são ingeridos nas variáveis de eventos do fluxo de trabalho e podem ser usados no fluxo de trabalho. Consulte a [documentação](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) de todas as atividades que podem ser personalizadas com variáveis de evento:

   * Configure a Atividade de teste (nova em 19.2)
   * Configurar Audiência de leitura e Atividade de Delivery por email

1. **Configurar uma Atividade** End para chamar um fluxo de trabalho com parâmetros externos

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Recursos adicionais

* [Sinal externo (documentação)](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
