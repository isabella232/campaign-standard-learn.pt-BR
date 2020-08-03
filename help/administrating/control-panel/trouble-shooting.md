---
title: Problemas ao tirar o Painel de controle do Campaign
description: O Painel de controle do Campaign permite que você monitore e gerencie seu armazenamento SFTP por instância e endereços IP de lista de permissões.
feature: Control Panel
topics: null
kt: 2938
doc-type: article
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 2f0527f3d9e2248eea68079e00855cce7a96fce4
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# Problema ao fotografar o [!UICONTROL Painel de controle do Campaign}

Saiba como solucionar problemas ao usar o Painel de controle do Campaign.

## Logon e página inicial

Problemas que ocorrem com o logon e a página inicial.

### Sintoma: Não é possível fazer logon no Adobe Experience Cloud

**O que fazer:**
O usuário precisa localizar seus [!DNL IMS Org ID] (xxx). O administrador precisa adicionar o usuário ao [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] para cada instância que ele deseja gerenciar. Se o usuário for um administrador de todas as instâncias, ainda será necessário adicioná-lo como *[!UICONTROL user]*.

### Sintoma: Os links no [!UICONTROL Adobe Experience Cloud Home] para acesso [!UICONTROL Control Panel] não aparecem para um usuário

**Causa:**
Os usuários não verão os links até que sejam adicionados como usuários a [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**O que fazer:**
O administrador precisa adicionar o usuário ao [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* para cada instância que ele deseja gerenciar. Se o usuário for um administrador de todas as instâncias, ainda será necessário adicioná-lo como *[!UICONTROL user]*.

### Sintoma: Uma Instância não está listada no [!UICONTROL Control Panel]

**Causa:**
Provavelmente, o usuário precisa ser adicionado como um Perfil *[!UICONTROL user]* de Produto `!DNL Campaign-xxx-Administrators/Admin` para a instância que está faltando

**O que fazer:**
O administrador precisa adicionar o usuário ao Perfil do Produto `Campaign-xxx-Admins` para cada instância que ele deseja gerenciar. Se o usuário for um administrador de todas as instâncias, ainda será necessário adicioná-lo como *[!UICONTROL user]*.

### Vídeos úteis

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)
*Verificação[!DNL IMS Org ID](00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)
*Como adicionar um administrador ao[!UICONTROL product profile]para *[!DNL administrators]*poder usar[!UICONTROL Control Panel](01:03 min)*

### Documentação útil

* [Descubra o [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-overview.html)
* [Gerenciamento de permissões para o [!UICONTROL Control Panel]](https://helpx.adobe.com/campaign/kb/control-panel-access.html)

## Estabelecendo conexão com o servidor SFTP (cliente ou API)

A conexão com servidores SFTP requer:

* [!UICONTROL allow listing] o endereço IP do qual você está se conectando ao servidor SFTP
* Par de chave privada/pública que precisa ser registrado com Adobe Campaign
* Se você se conectar diretamente ao servidor SFTP, também precisará do software cliente SFTP

### Documentação útil

* [Fazer logon no servidor SFTP](https://helpx.adobe.com/campaign/kb/control-panel-sftp.html#LoggingintoyourSFTPserver)

