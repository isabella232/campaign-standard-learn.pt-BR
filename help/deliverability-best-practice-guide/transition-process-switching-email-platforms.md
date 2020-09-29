---
title: Processo de transição - Alternar plataformas de email
description: 'Ao mover provedores de serviço de e-mail (ESPs), não é possível também transição seus endereços IP existentes e estabelecidos. É importante que você siga as práticas recomendadas para desenvolver uma reputação positiva ao começar novamente. Como os novos endereços IP que você usará ainda não têm reputação, os ISPs não podem confiar totalmente nos e-mails que vêm deles e precisam ter cautela no que eles permitem que sejam entregues aos seus clientes. '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---


# Processo de transição - Alternar plataformas de email

Ao mover provedores de serviço de e-mail (ESPs), não é possível também transição seus endereços IP existentes e estabelecidos. É importante que você siga as práticas recomendadas para desenvolver uma reputação positiva ao começar novamente. Como os novos endereços IP que você usará ainda não têm reputação, os ISPs não podem confiar totalmente nos e-mails que vêm deles e precisam ter cautela no que eles permitem que sejam entregues aos seus clientes.

Pense no que você faz quando encontra alguém novo. Normalmente, é necessário criar confiança em vez de confiá-los imediatamente. Não pense que sua marca ajudará automaticamente com essa confiança, porque os spammers usarão seu nome para fazer coisas ruins. Os ISPs precisam reavaliar suas práticas de envio, já que a ação é mais reveladora na entrega por email.

Estabelecer uma reputação positiva é um processo. Mas uma vez estabelecido, pequenos indicadores negativos terão menos impacto para você e para seu delivery de e-mail.

![O processo de transição](assets/transition-process.png)

O tempo necessário para aquecer seus endereços IP e domínios pode variar, mas um benchmark de até oito semanas é comum para remetentes típicos estabelecerem uma reputação no máximo em ISPs de nível 1 ([!DNL Gmail], [!DNL Microsoft], [!DNL Verizon]/[!DNL Yahoo]/[!DNL AOL], etc.).
Nas próximas seções, investigaremos algumas áreas principais para nos concentrarmos adequadamente na integração.

## Infraestrutura

O sucesso na entrega depende de uma base sólida. A infraestrutura de e-mail é um elemento principal. Uma infraestrutura de email construída corretamente inclui vários componentes. ou seja, domínio(s) e endereço(s) IP. Esses componentes são como a maquinaria por trás dos emails que você envia, e muitas vezes são a âncora do envio da reputação. Os consultores de entrega asseguram que esses elementos sejam configurados corretamente durante a implementação, mas, devido ao elemento de reputação, é importante que você tenha essa compreensão básica.

### Configuração e estratégia de domínio

Os tempos mudaram e alguns ISPs (como [!DNL Gmail] e [!DNL Yahoo]) agora incorporam a reputação do domínio como um ponto adicional quando se trata de anexar a reputação do email a um remetente. A reputação do seu domínio baseia-se no seu domínio de envio em vez do seu endereço IP. Isso significa que sua marca tem prioridade quando se trata de decisões de filtragem ISP.

Parte do processo de integração para novos remetentes no Adobe Campaign inclui a configuração dos domínios de envio e a garantia de que sua infraestrutura seja estabelecida corretamente. Você deve trabalhar com um especialista em quais domínios você planeja usar a longo prazo. Estas são algumas dicas que moldam uma boa estratégia de domínio:

* Seja o mais claro e reflexivo possível da marca com o domínio escolhido para que os usuários não identifiquem incorretamente o email como spam. Alguns exemplos são [!DNL newsletter.foo.com], [!DNL receipts.foo.com]e assim por diante.
* Você não deve usar seu domínio pai ou corporativo, pois isso pode afetar o delivery de e-mails de sua organização para ISPs.
* Considere usar um subdomínio do seu domínio pai para legitimar seu domínio de envio.
* Separe seus subdomínios para categorias de mensagens transacionais e de marketing. Isso ajudará seu fluxo de tráfego de email de forma mais confiável, à medida que os ISPs procurarem esse método de envio, que é uma prática recomendada para email e altamente recomendada.

### Estratégia de IP

É importante formar uma estratégia de IP bem estruturada para ajudar a estabelecer uma reputação positiva. O número de IPs e a configuração variam dependendo do modelo de negócios e das metas de marketing. Trabalhar com um especialista para desenvolver uma estratégia clara para o start do direito. Considere estes aspectos que são importantes notar:

* Muitos IPs podem causar problemas de reputação, já que é uma tática comum de spammers a snowshoe, que é uma tática usada por spammers onde o tráfego é espalhado por muitos IPs para maximizar o delivery de correio publicitário não solicitado. Mesmo que você não seja um spammer, pode parecer um se usar muitos IPs, especialmente se esses IPs não tiverem tráfego anterior.
* Poucos IPs podem causar problemas de throughput e possivelmente causar problemas de reputação. A throughput varia de acordo com o ISP. O quanto e a rapidez que um ISP está disposto a aceitar é geralmente baseado em sua infraestrutura e no envio de limites de reputação.
* A separação do tráfego para tipos de mensagens é fundamental. É importante, no mínimo, separar o marketing e o correio transacional em pools de IP separados.
* Dependendo da sua estratégia de email, pode ser aconselhável separar diferentes produtos ou fluxos de marketing em diferentes pools de IP se a sua reputação for drasticamente diferente. Alguns comerciantes também segmentam por região. A separação do IP para o tráfego com uma reputação mais baixa não corrigirá o problema de reputação, mas evitará problemas com seus &quot;bons&quot; delivery de email de reputação. Afinal, você não quer sacrificar sua boa audiência por uma mais arriscada.

### Loops de feedback

Nos bastidores, a Adobe Campaign está processando dados relacionados a rejeições, reclamações, cancelamento de assinaturas e muito mais. A configuração desses loops de feedback é um aspecto importante para a capacidade de entrega. As reclamações podem danificar a reputação, portanto, você deve remover endereços de e-mail que registram as reclamações da audiência do público alvo. É importante observar que [!DNL Gmail] não fornece esses dados de volta. Os cabeçalhos de cancelamento de inscrição de listas e a filtragem de envolvimento são especialmente importantes para [!DNL Gmail] os assinantes, que agora compõem a maioria das bases de dados de assinantes.

### Autenticação

Autenticação é o processo que os ISPs usam para validar a identidade de um remetente. Os dois protocolos de autenticação mais comuns são [!DNL Sender Policy Framework (SPF)] e [!DNL DomainKeys Identified Mail] (DKIM). Eles não estão visíveis para o usuário final, mas ajudam os ISPs a filtrar e-mails de remetentes verificados. [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC) está ganhando popularidade, embora suas políticas ainda não sejam incorporadas por todos os ISPs em seus sistemas de reputação.

#### **SPF**

[!DNL Sender Policy Framework (SPF)] é um método de autenticação que permite ao proprietário de um domínio especificar quais servidores de email eles usam para enviar emails desse domínio.

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] é um método de autenticação usado para detectar endereços de remetente forjados (comumente chamado [!DNL spoofing]). Se o DKIM estiver ativado, ele permitirá que o receptor confirme se o remetente está autorizado a enviar emails desse domínio.

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] é um método de autenticação que dá aos proprietários de domínio a capacidade de proteger seus domínios contra uso não autorizado. O DMARC usa SPF ou DKIM ou ambos para permitir que o proprietário de um domínio controle o que acontece com o email que falha na autenticação: entregues, em quarentena ou rejeitadas.

## Critérios de definição de metas

Ao enviar novo tráfego, apenas público alvo seus usuários mais comprometidos durante as fases iniciais do aquecimento de IP. Isso ajuda a estabelecer uma reputação positiva do get-go para efetivamente criar confiança antes de rodar em suas audiências menos comprometidas. Esta é uma fórmula básica para envolvimento:

![Fórmula para envolvimento](assets/formula-for-enagement.png)

Normalmente, uma taxa de envolvimento é baseada em um período específico. Essa métrica pode variar drasticamente dependendo se a fórmula for aplicada em um nível geral ou para tipos de correspondência ou campanhas específicos. Os critérios de definição de metas específicos precisam ser fornecidos trabalhando com seu consultor de entrega da Adobe Campaign, já que cada remetente e ISP varia e geralmente requer um plano personalizado.

## Considerações específicas de ISP durante o aquecimento de IP

Os provedores de internet têm regras diferentes e maneiras diferentes de ver seu tráfego. Por exemplo, [!DNL Gmail] é um dos ISPs mais sofisticados porque eles consideram o envolvimento de forma muito estrita (abre e clica) além de todas as outras medidas de reputação. Isso requer um plano personalizado que apenas público alvo os usuários mais envolvidos no início. Outros ISPs também podem exigir o mesmo. Trabalhe com seu consultor de entrega da Adobe Campaign para obter um plano específico.

## Volume

O volume de correio que você está enviando é essencial para estabelecer uma reputação positiva. Ponha-se nos sapatos dos ISPs. se você start ver um monte de tráfego de alguém que você não conhece, seria alarmante. Enviar imediatamente um grande volume de e-mails é arriscado e certamente causa problemas de reputação que muitas vezes são difíceis de resolver. Pode ser frustrante, demorado e caro para se livrar de problemas de má reputação, intimidação e bloqueio resultantes do envio muito em breve.

Os limites de volume variam de acordo com o ISP e também podem variar dependendo das métricas médias de envolvimento. Alguns remetentes requerem uma elevação de volume muito baixa e lenta, enquanto outros podem permitir uma subida de volume mais acentuada. Recomendamos trabalhar com um especialista, como um consultor de entrega da Adobe Campaign, para desenvolver um plano de volume personalizado.

Veja uma lista de dicas e dicas para saber como transição sem problemas:

* **A permissão** é a base de qualquer programa de email bem-sucedido.
* **Start** baixo e lento com baixos volumes de envio e aumento à medida que você estabelece a reputação do remetente.
* Uma estratégia **de envio de** tandem permite aumentar o volume de Campanha ao encerrar com seu ESP atual, sem interromper seu calendário de email.
* **Questões** de envolvimento - start com os assinantes que abrem e clicam em seus emails regularmente.
* **Siga o plano** — nossas recomendações ajudaram centenas de clientes Campanhas a aumentar seus programas de e-mail com sucesso.
* **Monitore sua conta** de email de resposta. É uma má experiência para o cliente usar [!DNL nore-ply@xyz.com] ou não responder.
* Endereços inativos podem ter um impacto negativo na entrega. **Reative e reautorize** na plataforma atual, não nos novos IPs.
* **Domínios** - use um domínio de envio que seja um subdomínio do domínio real da sua empresa. Por exemplo, se o domínio de empresa for [!DNL xyz.com], [!DNL email.xyz.com] fornecerá mais credibilidade aos ISPs do que [!DNL xyzemail.com]
* **Transparência** - os detalhes de registro do seu domínio de email devem estar disponíveis publicamente e não devem ser privados.

Em muitas circunstâncias, o correio transacional não segue a abordagem tradicional de aquecimento promocional. É obviamente difícil controlar o volume de emails transacionais devido à sua natureza, pois geralmente requer uma interação do usuário para acionar o toque de email. Em alguns casos, o correio transacional pode simplesmente ser transferido sem um plano formal. Em outros casos, pode ser melhor transição cada tipo de mensagem ao longo do tempo para aumentar lentamente o volume. Por exemplo, você pode desejar transição da seguinte maneira:

1. Confirmações de compra - alto envolvimento em geral
2. Desistência do carrinho - participação média-alta, em geral
3. E-mails de boas-vindas - alto envolvimento, mas pode conter endereços inválidos dependendo dos métodos de coleta de listas
4. E-mails de retorno - participação mais baixa geralmente

## Recursos adicionais

* [Iniciar uma nova plataforma](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)
