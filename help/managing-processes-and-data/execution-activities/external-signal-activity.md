---
title: Atividade de sinal externo - Chame um fluxo de trabalho com parâmetros
description: '"Saiba como iniciar um fluxo de trabalho a partir de outro para oferecer suporte a jornadas de clientes mais complexas, além de monitorar e reagir melhor aos problemas."'
feature: Execution Activity
topics: Workflows
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: Business Practitioner, Developer
level: Experienced
translation-type: tm+mt
source-git-commit: 5d2bc8bd3a3a0fdb5e2f1ef75af2ab60b8f6abc8
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ]- Chamar um fluxo de trabalho com parâmetros

O [!UICONTROL External Signal activity] é usado para organizar e orquestrar diferentes processos que fazem parte da mesma jornada do cliente em workflows diferentes. Ele permite iniciar um workflow a partir de outro, permitindo oferecer suporte a jornadas de clientes mais complexas, além de poder monitorar e reagir melhor em caso de problemas.

No ACS 19.2, o [!UICONTROL External Signal activity] não só pode chamar um workflow, como também pode enviar parâmetros para o workflow (um nome de público-alvo para o target, um nome de arquivo a ser importado, uma parte do conteúdo da mensagem etc.) para o workflow a partir de outro workflow ou de uma chamada à API REST para integração com seus sistemas externos.

Isso também inclui uma nova Atividade **Test**, na qual você pode executar testes nesta funcionalidade.

O vídeo a seguir explica as etapas de configuração necessárias para:

1. **Receba** parâmetros externos de um sistema externo, como um CRM (Content Management System, sistema de gerenciamento de conteúdo):

   * Declarar os parâmetros na Atividade de sinal externo
   * Configure a chamada da API para definir os parâmetros e acionar a Atividade do sinal externo do workflow. Para obter mais informações sobre como configurar uma chamada de API, consulte [Acionando uma atividade de sinal](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Personalize um workflow com parâmetros externos**  (variáveis de eventos):

   Depois que o workflow é acionado, os parâmetros são assimilados nas variáveis de eventos do workflow e podem ser usados dentro dele. Consulte a [documentação](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) para todas as atividades que podem ser personalizadas com variáveis de evento:

   * Configurar a atividade de teste (nova em 19.2)
   * Configurar Atividade Ler Público-Alvo e Delivery de Email

1. **Configure uma atividade End** para chamar um workflow com parâmetros externos

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Recursos adicionais

* [Sinal externo (documentação)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
