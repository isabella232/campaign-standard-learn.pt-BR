---
title: Solicitações de privacidade com o Adobe Campaign Standard (ACS) - Visão geral
description: O tutorial explica como criar solicitações de privacidade por meio da interface do Adobe Campaign Standard (ACS).
feature: GDPR, CCAP
topic: Privacidade
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '371'
ht-degree: 100%

---


# Solicitações de privacidade com a interface do Adobe Campaign Standard

O Adobe Campaign oferece aos controladores de dados três métodos para executar o acesso à Privacidade e excluir solicitações de dados PII em conformidade com as leis de privacidade, como o GDPR (Regulamento Geral sobre a Proteção de Dados) e a CCPA (Lei de Privacidade do Consumidor da Califórnia):

* **Pela integração do Serviço principal de privacidade:** as solicitações de privacidade transmitidas do [!UICONTROL Privacy Service] para todas as soluções da Experience Cloud são tratadas automaticamente pelo Campaign, por meio de um fluxo de trabalho específico. Consulte o [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) para saber como criar solicitações de privacidade no Serviço principal de privacidade

* **Pela API:** o Adobe Campaign fornece uma API que permite o processo automático de solicitações de privacidade usando REST

* **Pela interface do Adobe Campaign:** para cada solicitação de acesso a dados pessoais, o controlador de dados cria uma nova solicitação de acesso a dados pessoais no Adobe Campaign

>[!NOTE]
>
> **ALTERAÇÕES NO ACS 19.4:**
> 
> A [Integração do Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) é o método que deve ser usado para todas as solicitações de acesso e exclusão. A partir da versão 19.4, o uso da API e da interface do Campaign para solicitações de acesso e exclusão se tornará obsoleto. Para obter mais informações sobre recursos obsoletos e removidos do Campaign Standard, consulte [esta página](https://helpx.adobe.com/br/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Recusar a venda de informações pessoais (CCPA)**
>
>A partir da versão 19.4, o campo Recusa da CCPA é oferecido pronto para uso na interface e API do Campaign. Para usar essas informações na versão 19.3, é necessário criar esse campo no Adobe Campaign Standard. Consulte a [documentação detalhada](https://helpx.adobe.com/br/campaign/kb/acs-privacy.html#ccpa) para obter mais informações.
>
> Você pode verificar sua versão clicando no ícone ? no canto superior direito da interface e selecionando Sobre.

## Tutoriais em vídeo

### Pré-requisitos para solicitações de privacidade

1. [Criar um namespace](/help/privacy/namespaces-for-privacy-requests.md)
1. [Modificar recursos personalizados](/help/privacy/custom-resources-for-privacy-requests.md)

### Criar, rastrear e executar solicitações de privacidade por meio da interface do usuário do Adobe Campaign

* [Criar e rastrear solicitações de privacidade por meio da interface do usuário do Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Executar solicitações de privacidade](/help/privacy/execute-privacy-requests.md)

## Recursos adicionais

* [Diretrizes gerais de privacidade do Campaign](https://helpx.adobe.com/br/campaign/kb/campaign-privacy-overview.html)
* [CCPA para ACS](https://helpx.adobe.com/br/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Documentação da API REST do Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
