---
title: Solução de problemas do Painel de controle do Campaign
description: O Painel de controle do Campaign permite monitorar e gerenciar o armazenamento SFTP por instância e lista de permissões endereços IP de .
feature: Painel de controle do Campaign
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# Resolução de problemas do [!UICONTROL Control Panel]

Saiba como solucionar problemas do Painel de controle do Campaign.

## Logon e página inicial

Problemas com o logon e a página inicial.

### Sintoma: Não é possível fazer logon no Adobe Experience Cloud

**O que fazer:**
O usuário deve localizar seus  [!DNL IMS Org ID] (xxx). O administrador deve adicionar o usuário ao [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ele deverá se adicionar como *[!UICONTROL user]*.

### Sintoma: os links no [!UICONTROL Adobe Experience Cloud Home] para acessar o [!UICONTROL Control Panel] não aparecem para um usuário

**Causa:**
Os usuários não verão os links até que sejam adicionados como usuários ao [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**O que fazer:**
O administrador deve adicionar o usuário ao  [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ele deverá se adicionar como *[!UICONTROL user]*.

### Sintoma: uma instância não está listada no [!UICONTROL Control Panel]

**Causa:**
Provavelmente, o usuário deve ser adicionado como um Perfil  *[!UICONTROL user]* de Produto  `Campaign-xxx-Administrators/Admin` para a instância que está ausente

**O que fazer:**
O administrador deve adicionar o usuário ao Perfil de produto  `Campaign-xxx-Admins` para cada instância que ele quiser gerenciar. Se o usuário for um administrador de todas as instâncias, ele deverá se adicionar como *[!UICONTROL user]*.

### Vídeos úteis

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Verificação [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Como adicionar um administrador ao [!UICONTROL product profile] [!DNL administrators] para poder usar o [!UICONTROL Control Panel] (01:03 min)*

### Documentação útil

* [Descubra o [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=pt-BR)
* [Gerenciamento de permissões para o [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## Estabelecer conexão com o servidor SFTP (cliente ou API)

A conexão com servidores SFTP requer:

* [!UICONTROL allow listing] o endereço IP a partir do qual você está se conectando ao servidor SFTP
* Par de chave privada/pública que deve ser registrado no Adobe Campaign
* Se você se conectar diretamente ao servidor SFTP, precisará de software cliente SFTP

### Documentação útil {#helpful-docs}

* [Fazer logon no servidor SFTP](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
