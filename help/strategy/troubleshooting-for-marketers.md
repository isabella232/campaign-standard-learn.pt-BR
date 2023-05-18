---
title: Solução de problemas para profissionais de marketing
description: Conhecer os erros mais comuns pode ajudar na solução mais rápida de problemas e aumentar sua produtividade. Essas dicas de solução de problemas ajudam você a resolver com eficácia erros semelhantes à medida que ocorrem.
version: Standard
feature: Workflows
role: User
level: Beginner, Intermediate, Experienced
doc-type: Article
last-substantial-update: 2023-05-18T00:00:00Z
jira: KT-13256
thumbnail: KT-13256.jpeg
source-git-commit: f7f2b6abb26075b25a3b55e4ceed744172691ce8
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 1%

---


# Solução de problemas para profissionais de marketing: 5 Erros comuns de workflow e delivery

Por: [Suraj Patra](https://www.linkedin.com/in/suraj-p-51612053/){target="_blank"}, Consultor Sênior, Meijer

Como engenheiro sênior e especialista em produtos da Adobe Experience Cloud nos últimos cinco anos, eu habilito usuários empresariais no [Meijer](https://www.meijer.com/){target="_blank"}, uma cadeia de supercentros norte-americana criada em 1934 para realizar campanhas complexas e de marketing e transacionais com ACS. Alguns projetos nos quais trabalhei incluem campanhas personalizadas para armazenar ofertas e detalhes de pedidos para personalização, integradas ao Adobe Audience Manager e insight do cliente para assimilação de segmento.


No meu tempo usando o ACS, encontrei erros que podem ser demorados e frustrantes para resolver. Conhecer os erros mais comuns pode ajudar na solução mais rápida de problemas e aumentar sua produtividade. Abaixo estão minhas dicas de solução de problemas para ajudá-lo a resolver com eficácia erros semelhantes que ocorrem.

## Erro de Incompatibilidade de Tipo de Dados

**Código de erro:**
`PGS-220000 PostgreSQL error: ERROR: operator does not exist: character varying = bigint`

**Causa:**
Esses tipos de erros aparecem em um workflow quando você tenta reconciliar usando campos de tipos de dados diferentes. Por exemplo, ao fazer upload de um arquivo usando um arquivo de carregamento que tem um campo de string, você tenta reconciliar o campo de string com um campo de perfil que tem um tipo de dados int.

![data-type-mismatch-error](/help/assets/kt-13256/data-type-mismatch.png)

**Solução:**
Altere o tipo de dados do campo na atividade &quot;Carregar arquivo&quot; para aquele com o qual você está correspondendo. Abra a atividade &quot;Carregar arquivo&quot;. Mova para a guia &quot;DEFINIÇÃO DE COLUNA&quot; e altere o tipo de dados do campo desejado.


![solução de incompatibilidade de tipo de dados](/help/assets/kt-13256/data-type-mismatch-solution.png)

## Erro de personalização do delivery

**Código de erro:**
`The schema for profiles specified in the transition ('') is not compatible with the schema defined in the delivery template ('nms:recipient'). They should be identical.`

**Causa:**
Este erro aparece quando você está enviando um email para um endereço, mas o email ou qualquer outro identificador não é reconciliado com um perfil. Para enviar uma comunicação por email, o email ou o identificador deve estar sempre vinculado a um perfil.

Use a atividade de reconciliação conforme mostrado abaixo:

![workflow com atividade de reconciliação](/help/assets/kt-13256/del-persn-error-wf.png)

**Solução:**
Uma ID comum deve existir no arquivo carregado com a tabela de recipients. Essa chave comum junta o arquivo de carregamento à tabela do recipient na atividade de reconciliação. Os emails não podem ser enviados para registros que não existem na tabela de recipients que requer essa etapa de reconciliação no workflow. Ao fazer isso, reconcilie a atividade de carregamento de arquivo de entrada com um identificador como ID de email do perfil. O `nms:recipient` schema se refere à tabela de perfis e a reconciliação dos registros recebidos com o perfil a torna disponível durante a preparação do email.

Consulte a captura de tela para obter a atividade de reconciliação, conforme mostrado abaixo.

![fluxo de trabalho com detalhes de reconciliação](/help/assets/kt-13256/del-persn-error-wf-solution.png)

Saiba mais sobre [reconciliação](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/data-management-activities/reconciliation.html?lang=en).

## Erro de Conjunto de Dados de Campo Comum

**Código de erro:**
`The document types of inbound events (''and'') are incompatible (step 'Exclusion'). Unable to perform the operation. `

**Causa:**
Esse problema ocorre ao usar a variável **atividade de exclusão** em workflows ACS. O erro ocorre ao executar e excluir com base na ID, quando o conjunto Principal e o conjunto excluído não têm os mesmos nomes de campo.


![Erro de Conjunto de Dados de Campo Comum](/help/assets/kt-13256/dataset-error.png)

**Solução:**

Há duas maneiras de resolver esse erro:

1. Use o mesmo nome de campo no primário e no excluído e use esse campo como ID

   OU

1. Use o método de exclusão JOINS para selecionar o campo com base no qual deseja excluir os registros.

![Erro de Conjunto de Dados de Campo Comum - Solução ](/help/assets/kt-13256/dataset-error-solution.png)

## Erro de soltar nome do campo

**Código de erro:**
`XTK-170036 Unable to parse expression 'i__name'`

**Causa:**

Pontos de falha podem ocorrer em um **atividade de enriquecimento**. Um dos mais comuns é exibido abaixo.

![Erro de soltar nome do campo](/help/assets/kt-13256/field-name-dropped-error.png)

Isso acontece quando você edita manualmente um nome de expressão na atividade. A imagem mostra que a expressão foi modificada de `name `para `i__name`.

**Solução:**

Você pode resolver esse erro de três maneiras:

1. Altere o nome de volta para a expressão que estava originalmente presente.

2. Se quiser usar um novo nome, altere os valores no **atividade de enriquecimento**.

3. Se você não se lembrar do que mudou, sua melhor aposta seria recriar a atividade.

## Erro de queda de tabela temporária 

**Código de erro:**
`XTK-170024 The temporary schema "temp:deliveryEmail1" is not defined in the current context.`

**Causa:**
Este é um erro comum em workflows complicados envolvendo enriquecimento ou outra atividade. Provavelmente, significa que alguns dos workflows da atividade não são salvos corretamente durante várias alterações no workflow.

![Erro de queda de tabela temporária ](/help/assets/kt-13256/temp-table-dropped-error.png)

**Solução:**
Existem muitas maneiras de esse erro ocorrer, de modo que não há uma correção simples. Se for um fluxo de trabalho simples, é melhor reconfigurar a atividade. Em um workflow complicado, é melhor copiar as atividades do workflow para um novo workflow, salvá-lo e executá-lo novamente.