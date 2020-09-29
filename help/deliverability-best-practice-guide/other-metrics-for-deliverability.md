---
title: Outras métricas importantes para a entrega
description: Uma das melhores maneiras de identificar um problema de reputação de envio é através das métricas. Vamos analisar algumas métricas principais de entrega para monitorar e como usá-las para identificar um problema de reputação.
feature: null
topics: Deliverability
kt: 5256
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 7aa32d583ac2ea756945a17634fb477d7b94cb7f
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 1%

---


# Outras métricas importantes para a entrega

Uma das melhores maneiras de identificar um problema de reputação de envio é através das métricas. Vamos analisar algumas métricas principais de entrega para monitorar e como usá-las para identificar um problema de reputação.

## Rejeições

Rejeições são o resultado de uma tentativa de delivery e falha em que o ISP fornece avisos de falha. O processamento de tratamento de rejeição é uma parte essencial da higiene das listas. Depois que um determinado email saltou várias vezes seguidas, esse processo o sinaliza para supressão. O número e o tipo de rejeições necessários para acionar a supressão variam de sistema para sistema. Esse processo impede que os sistemas continuem a enviar endereços de email inválidos. Rejeições são um dos principais dados que os ISPs usam para determinar a reputação do IP. Manter um olho nessa métrica é muito importante. &quot;Entregue&quot; versus &quot;saltado&quot; é provavelmente a maneira mais comum de medir o delivery das mensagens de marketing: quanto maior a porcentagem entregue, melhor. Vamos cavar em dois tipos diferentes de rejeições.

## Devoluções permanentes

As rejeições em disco rígido são falhas permanentes geradas depois que um ISP determina uma tentativa de envio por correio para um endereço de assinante como não entregável. No Adobe Campaign, rejeições em disco que são categorizadas como não entregues são adicionadas à quarentena, o que significa que elas não seriam tentadas novamente. Há alguns casos em que uma rejeição forçada seria ignorada se a causa da falha fosse desconhecida. Estes são alguns exemplos comuns de rejeições forçadas:

* O endereço não existe
* Conta desabilitada
* Sintaxe incorreta
* Domínio incorreto

## Devoluções temporárias

Rejeições suaves são falhas temporárias que os ISPs geram quando têm dificuldade em entregar correio. As falhas de software serão repetidas vezes (com variação dependendo do uso de configurações personalizadas ou predefinidas do delivery Adobe Campaign) para tentar um delivery bem-sucedido. Endereços que continuamente rejeitam não serão adicionados à quarentena até que o número máximo de tentativas tenha sido tentado (o que novamente varia dependendo das configurações). Algumas causas comuns de rejeições de software incluem:

* Caixa de entrada cheia
* A receber servidor de correio eletrônico para baixo
* Problemas de reputação do remetente

![tipos de rejeição](assets/bounce-types.png)

>[!NOTE]
>
>Rejeições são um indicador chave de um problema de reputação, pois podem destacar uma fonte de dados inválida (rejeição) ou um problema de reputação com um ISP (rejeição parcial).
Geralmente, as rejeições de software ocorrem como parte do envio de e-mail e devem ser permitidas resolvê-las durante o processamento da nova tentativa antes de caracterizar como um problema de entrega real. Se a sua taxa de rejeição flexível for maior que 30% para um único ISP e não for resolvida dentro de 24 horas, é recomendável levantar uma preocupação com seu consultor de entrega da Adobe Campaign.

## Reclamações

As reclamações são registradas quando um usuário indica que um email é indesejado ou inesperado. Normalmente, essa ação do assinante é registrada pelo cliente de e-mail do assinante quando ele aperta o botão de spam ou por um sistema de relatórios de spam de terceiros.

### Queixa ISP

A maioria dos ISPs de nível 1 e alguns de nível 2 fornecem um método de relatórios de spam para seus usuários, já que os processos de cancelamento de inscrição e cancelamento de inscrição foram usados de forma maliciosa no passado para validar um endereço de email. A Adobe Campaign recebe essas reclamações por meio de FBLs ISP. Isso é estabelecido durante o processo de configuração para todos os ISPs que fornecem FBLs e permite que a Adobe Campaign adicione automaticamente endereços de email que reclamaram para a tabela de quarentena para supressão. Os picos nas reclamações de ISP podem ser um indicador de baixa qualidade de lista, métodos de coleta de listas que não são ótimos ou políticas de envolvimento fracas. Elas também são observadas com frequência quando o conteúdo não é relevante.

### Queixas de terceiros

Há vários grupos antisspam que permitem relatórios de spam em um nível mais amplo. As métricas de reclamação usadas por esses terceiros são usadas para marcar conteúdo de email para identificar email de spam. Esse processo também é conhecido como impressão digital. Os usuários desses métodos de reclamação de terceiros geralmente são mais seguros com relação ao email, portanto, podem ter um impacto maior do que outras reclamações podem ter se não respondidas.

>[!NOTE]
>
>Os ISPs coletam reclamações e as usam para determinar a reputação geral de um remetente. Todas as queixas devem ser suprimidas e deixadas de ser contactadas o mais rapidamente possível e de acordo com as leis e regulamentos locais.

## Armadilhas de spam

Uma armadilha de spam é um endereço usado para identificar um email não solicitado ou não permitido. Existem armadilhas de spam para ajudar a identificar emails de remetentes fraudulentos ou que não seguem as práticas recomendadas de email. O endereço de email da captura de spam geralmente não é publicado publicamente e é quase impossível de identificar. A entrega de e-mails para armadilhas de spam pode afetar sua reputação com diversos graus de gravidade, dependendo do tipo de armadilha e do ISP. Saiba mais sobre os diferentes tipos de armadilhas de spam nas seções a seguir.

### Reciclado

As armadilhas de spam reciclado são endereços válidos uma vez, mas que não estão mais sendo usados. Uma maneira importante de manter o lista o mais limpo possível é enviar e-mails regularmente para toda a sua lista e suprimir adequadamente e-mails enviados. Isso ajuda os endereços de e-mail abandonados a serem colocados em quarentena e retidos do uso posterior.

Em alguns casos, um endereço pode ser reciclado dentro de 30 dias. O envio regular é um aspecto vital da boa higiene das listas, juntamente com a supressão regular dos utilizadores inativos. As campanhas de retomada de participação normalmente são parte de programas sofisticados de marketing por email. Esse estilo de campanha permite que o remetente tente recuperar usuários que, de outra forma, não seriam mais enviados por email.

### Typo

Uma armadilha de spam de erro de digitação é um endereço que contém erros ortográficos ou malformações. Isso geralmente ocorre com erros ortográficos conhecidos de domínios principais, como [!DNL Gmail] (por exemplo: [!DNL gmail] o ad um erro de digitação frequente). Os ISPs e outros operadores de lista de blocos registrarão domínios inválidos conhecidos para serem usados como armadilhas de spam, a fim de identificar remetentes de spam e medir a integridade do remetente. A melhor maneira de evitar armadilhas de spam de erro de digitação é usar um processo de aceitação de duplo para a coleção de listas.

### Pristina

Uma armadilha de spam inigualável é um endereço que não tem usuário final e nunca teve um usuário final. É um endereço criado apenas para identificar e-mails de spam. Esse é o tipo mais impactante de armadilha de spam, já que é virtualmente impossível de identificar e exigiria um esforço substancial para limpar da sua lista. A maioria das listas negras utiliza armadilhas de spam inesquecíveis para lista de remetentes sem reputação. A única maneira de evitar que armadilhas de spam intocáveis infectem sua lista de email de marketing mais ampla é utilizar um processo de aceitação de duplo para a coleção de listas.

## Marcação

O bulking é o delivery de correio na pasta spam ou lixo eletrônico de um ISP. É identificável quando uma taxa aberta inferior ao normal (e às vezes a taxa de cliques) é emparelhada com uma taxa de entrega alta. As causas para os e-mails serem marcados variam de acordo com o ISP. No entanto, em geral, se forem colocadas mensagens na pasta de massa, um sinalizador que influencia o envio da reputação (higiene da lista, por exemplo) requer uma reavaliação. É um sinal de que a reputação está diminuindo, o que é um problema que precisa ser corrigido imediatamente antes de afetar outras campanhas. Entre em contato com seu consultor de fornecimento da Adobe Campaign para solucionar quaisquer problemas com marcadores, dependendo da sua situação.

## Bloqueio

Um bloqueio ocorre quando os indicadores de spam atingem limites de ISP proprietários e o ISP começa a bloquear o email (notável por meio de tentativas de mala direta) de um remetente. Há vários tipos de blocos. Geralmente, os blocos ocorrem especificamente para um endereço IP, mas também podem ocorrer no nível de domínio ou entidade de envio. A solução de um bloco exige uma experiência específica, portanto entre em contato com seu consultor de entrega da Adobe Campaign para obter assistência.

## Listas negras

Uma lista negra ocorre quando um gerente de lista negra de terceiros registra um comportamento semelhante ao de um remetente. A causa de uma lista negra é, às vezes, publicada pelo grupo que faz a lista negra. Uma listagem é geralmente baseada no endereço IP, mas em casos mais graves pode ser por intervalo IP ou até mesmo um domínio de envio. Resolver uma lista negra deve envolver o suporte do seu consultor de entrega da Adobe Campaign para resolver e impedir outras listas. Algumas listagens são extremamente graves e podem causar problemas de reputação de longa duração, que são difíceis de resolver. O resultado de uma lista negra varia de acordo com a lista negra, mas tem o potencial de afetar o delivery de todos os emails.

## Recursos adicionais

* [Tipos e motivos de falha de delivery](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/monitoring-messages/understanding-delivery-failures.html#delivery-failure-types-and-reasons)
