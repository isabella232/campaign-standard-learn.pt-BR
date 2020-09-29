---
title: Estratégia e definição de entregabilidade
description: A criação de campanhas bem-sucedidas de marketing por email depende de uma compreensão clara das metas de marketing, sejam elas de prospecção ou de iniciativas de gerenciamento de relacionamento com o cliente (CRM). Isso ajuda a determinar quem público alvo, o que promover e quando o alcance é ideal.
feature: null
topics: Deliverability
kt: 5255
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f797faaf9189f64eb6fc57b84c5e38d4418d5f51
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 11%

---


# Estratégia e definição de entregabilidade

A criação de campanhas bem-sucedidas de marketing por email depende de uma compreensão clara das metas de marketing, sejam elas de prospecção ou de iniciativas de gerenciamento de relacionamento com o cliente (CRM). Isso ajuda a determinar quem público alvo, o que promover e quando o alcance é ideal.

Estes são alguns exemplos de objetivos de estratégia de marketing de email:

* Adquirir novos clientes
* Converter prospectos em compradores pela primeira vez
* Relações cada vez maiores com os clientes atuais com ofertas adicionais de clientes
* Manutenção de clientes fiéis
* Melhorando a satisfação do cliente e a fidelidade à marca
* Reativação de clientes perdidos ou lapidados

## Disponibilidade definida

Há duas métricas principais que desempenham um papel na definição da capacidade de entrega. A taxa de entrega é a porcentagem de e-mails que não retornam e são aceitos pelo ISP. O próximo é o posicionamento da caixa de entrada, que é aplicado às mensagens aceitas pelo ISP e determina se o email chega na caixa de entrada ou na pasta de spam.

É importante entender a taxa de entrega e a taxa de colocação da caixa de entrada em conjunto uma com a outra ao medir o desempenho do email. Uma alta taxa de entrega não é a única faceta da entrega. Só porque uma mensagem é recebida por meio de um ponto de verificação inicial do ISP não significa necessariamente que seu assinante realmente viu e interagiu com sua comunicação.

## Por que a entrega é importante

Se você não sabe se seus e-mails estão sendo entregues ou se eles estão chegando na caixa de entrada e não na pasta de spam, você deve. Eis o porquê.

Inúmeras horas vão para o planejamento e a produção de suas campanhas de email. Se os e-mails saltarem ou, em última análise, chegarem à pasta de spam dos seus assinantes, seus clientes provavelmente não os lerão, sua chamada para ação (CTA) não será reconhecida e você ficará aquém das metas de receita devido a conversões perdidas. Simplificando, você não pode se dar ao luxo de ignorar a capacidade de entrega. É crucial para o sucesso de seus esforços de marketing por email — e seus resultados.

Seguir as práticas recomendadas de entrega garante que seu email tenha a melhor chance possível de abrir, clicar e atingir o objetivo final — a conversão. Você pode escrever uma linha de assunto brilhante e ter belas imagens e conteúdo envolvente. Mas se esse email não for entregue, o cliente não terá nenhuma oportunidade de conversão. Em suma, na entrega por e-mail, cada etapa do processo de aceitação de e-mail depende da primeira para o sucesso do programa.

### Etapa 1: Email entregue

Fatores importantes para o delivery:

* Infraestrutura sólida: Configuração de IP e domínio, configuração de loop de feedback (FBL) (incluindo monitoramento e processamento com-plaint) e processamento de rejeição regular. Para clientes Adobe Campaign, a Adobe é responsável por essa configuração em nome de nossos clientes.
* Autenticação forte: SPF (Sender Policy Framework), DKIM (DomainKeys Identified Mail), autenticação de mensagem baseada em domínio, Relatórios e conformidade (DMARC).
* Qualidade da lista elevada: Aceitação explícita, métodos válidos de aquisição de email e políticas de envolvimento.
* O envio consistente de cadência e a minimização das flutuações de volume.
* Alta reputação de IP e domínio.

### Etapa 2: Inserção da caixa de entrada de email

Os ISPs têm algoritmos únicos, complexos e em constante mudança para determinar se seu email é colocado na caixa de entrada ou na pasta de lixo eletrônico ou spam.
Estes são alguns fatores importantes para o posicionamento da caixa de entrada:

* Email entregue
* Alto envolvimento
* Baixas reclamações (menos de 0,1% no total)
* Volume consistente
* Baixas de spam
* Baixa taxa de rejeição em disco rígido
* Ausência de lista negra

### Etapa 3: Participação de email — abre

Estes são alguns fatores importantes para a taxa aberta:

* Email entregue e entregue na caixa de entrada
* Reconhecimento de marca
* Linha de assunto e pré-cabeçalhos
* Personalização
* Frequência
* Relevância ou valor do conteúdo

### Etapa 4: Participação no email — cliques

Estes são alguns fatores importantes para a taxa de cliques:

* Email entregue, colocado na caixa de entrada e aberto
* CTA forte
* Essa é a ação principal que você deseja realizar com sua audiência. Normalmente, é um clique em um URL. Certifique-se de que seja claro e fácil para o usuário encontrar.
* Relevância ou valor do conteúdo

### Etapa 5: Conversão

Estes são alguns fatores importantes para a conversão:

* Todos os itens acima
* Transição de e-mail via URL de trabalho para uma landing page ou página de vendas
* experiência landing page
* Reconhecimento de marca, percepção e fidelidade

### Impacto potencial na receita

A conversão é a chave, mas qual é a alternativa? Sua estratégia de entrega pode fortalecer ou causar estragos no programa de marketing por email nirvana. O gráfico a seguir ilustra a possível perda de receita que uma política fraca de entrega pode ter no seu programa de marketing. Como demonstrado, para uma empresa com uma taxa de conversão de 2% e compra média de US$ 100, cada redução de 10% na colocação na caixa de entrada equivale a uma perda de receita de quase US$ 20.000. Lembre-se de que esses números são exclusivos para cada remetente.

| Sent | Percent | Entregue | Percent | Caixa de entrada | Número não incluído na caixa de entrada | Taxa de conversão | Número de perdidos | Average | Perdido |
|------|-----------|-----------|----------|-------|---------------------|-----------------|-----------------|----------|-----------|
|  | entregues |  | caixa |  |  |  | Conversões | compra | receita |
| 100K | 99% | 99K | 100% | 99K | - | 2% | 0 | $100 | $ - |
| 100K | 99% | 99K | 90% | 89.1K | 9,900 | 2% | 198 | $100 | $19,800 |
| 100K | 99% | 99K | 80% | 79.2K | 19,800 | 2% | 396 | $100 | $39,600 |
| 100K | 99% | 99K | 70% | 69.3K | 29,700 | 2% | 594 | $100 | $59,400 |
| 100K | 99% | 99K | 60% | 59.4K | 39,600 | 2% | 792 | $100 | $79,200 |
| 100K | 99% | 99K | 50% | 49.5K | 49,500 | 2% | 990 | $100 | $99,000 |
| 100K | 99% | 99K | 40% | 39.6K | 59,400 | 2% | 1188 | $100 | $118,800 |
| 100K | 99% | 99K | 30% | 29.7K | 69,300 | 2% | 1386 | $100 | $138,600 |
| 100K | 99% | 99K | 20% | 19.8K | 79,200 | 2% | 1584 | $100 | $158,400 |

## Recursos adicionais
