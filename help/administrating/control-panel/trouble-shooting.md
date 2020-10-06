---
title: Solução de problemas do Painel de controle do Campaign
description: O Painel de controle do Campaign permite monitorar e gerenciar o armazenamento SFTP por instância e endereços IP na lista de permissões.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 66b8f4b6378eb974dc858b28c0479a9cb5d52a6b
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 100%

---


# Resolução de problemas do [!UICONTROL Control Panel]

Saiba como solucionar problemas do Painel de controle do Campaign.

## Logon e página inicial

Problemas com o logon e a página inicial.

### Sintoma: não é possível fazer logon na Adobe Experience Cloud

**O que fazer:**
O usuário precisa localizar seus [!DNL IMS Org ID] (xxx). O administrador precisa adicionar o usuário ao [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ainda assim será necessário adicioná-las como *[!UICONTROL user]*.

### Sintoma: os links no [!UICONTROL Adobe Experience Cloud Home] para acessar o [!UICONTROL Control Panel] não aparecem para um usuário

**Causa:**
Os usuários não verão os links até que sejam adicionados como usuários ao [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**O que fazer:**
O administrador precisa adicionar o usuário ao [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ainda assim será necessário adicioná-las como *[!UICONTROL user]*.

### Sintoma: uma instância não está listada no [!UICONTROL Control Panel]

**Causa:**
Provavelmente, o usuário precisa ser adicionado como um *[!UICONTROL user]* Perfil de Produto `Campaign-xxx-Administrators/Admin` para a instância que está ausente

**O que fazer:**
O administrador precisa adicionar o usuário ao Perfil de produto do `Campaign-xxx-Admins` para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ainda assim será necessário adicioná-las como *[!UICONTROL user]*.

### Vídeos úteis

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Verificação [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Como adicionar um administrador ao [!UICONTROL product profile] *[!DNL administrators]* para poder usar o [!UICONTROL Control Panel] (01:03 min)*

### Documentação útil

* [Descubra o [!UICONTROL Control Panel]](https://helpx.adobe.com/br/campaign/kb/control-panel-overview.html)
* [Gerenciamento de permissões para o [!UICONTROL Control Panel]](https://helpx.adobe.com/br/campaign/kb/control-panel-access.html)

## Estabelecer conexão com o servidor SFTP (cliente ou API)

A conexão com servidores SFTP requer:

* [!UICONTROL allow listing] o endereço IP a partir do qual você está se conectando ao servidor SFTP
* Par de chave privada/pública que precisa ser registrado com o Adobe Campaign
* Se você se conectar diretamente ao servidor SFTP, precisará também do software cliente SFTP

### Documentação útil

* [Fazer logon no servidor SFTP](https://docs.adobe.com/content/help/pt-BR/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)

