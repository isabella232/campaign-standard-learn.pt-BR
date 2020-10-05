---
title: Painel de controle do Campaign
description: O Painel de controle do Campaign permite monitorar e gerenciar o armazenamento SFTP por instância e endereços IP na lista de permissões.
feature: Control Panel
topics: Control Panel
kt: 4696
doc-type: feature video
activity: use
team: PM
translation-type: ht
source-git-commit: 906b1d76e4723b50e2d06f6525763bbd73b98e10
workflow-type: ht
source-wordcount: '364'
ht-degree: 100%

---


# [!UICONTROL Control Panel] {#control-panel}

>[!NOTE]
>
>Os termos &quot;[!UICONTROL whitelist]&quot; e &quot;[!UICONTROL blacklist]&quot; foram substituídos por &quot;[!UICONTROL allow list]&quot; e &quot;[!UICONTROL block list]&quot;na documentação do Adobe Campaign. Algumas ocorrências desses termos ainda podem existir na interface do usuário do produto, nomes de opções e código interno, bem como nos vídeos de tutoriais. Eles serão substituídos em versões futuras do Painel de controle do Campaign.

O [!UICONTROL Control Panel] permite que os administradores do Adobe Campaign monitorem os principais ativos e executem tarefas administrativas, como gerenciar o armazenamento SFTP por instância ou endereços IP do [!UICONTROL allow list].

## Acesso ao [!UICONTROL Control Panel]

Para acessar o Painel de controle do Campaign, vá até a página inicial da Experience Cloud: [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com):

* **[!UICONTROL Experience Cloud Home]** > **[!UICONTROL Quick Access]**

   ou
* **[!UICONTROL Experience Cloud Home]**  > [!UICONTROL Solution picker]: **Campaign** > **[!UICONTROL Control Panel]card**

   ou

* Diretamente pelo URL: [https://experience.adobe.com/#/controlpanel](https://experience.adobe.com/#/controlpanel)

## Pré-requisitos

Antes de começar, conclua os seguintes pré-requisitos:

### Confirmar o [!DNL IMS Org ID]

Você precisa conhecer o seu [!DNL IMS org ID]. O vídeo a seguir descreve onde você pode pesquisar o [!DNL IMS org ID] da sua instância.

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12&captions=por_br)
*Verificação[!DNL IMS Org ID](00:26 min)*

### Direitos de administrador

Os direitos de administrador são necessários para acessar o [!UICONTROL Control Panel].
O vídeo a seguir explica como adicionar um administrador a uma instância do Campaign

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12&captions=por_br)
*Como adicionar um administrador ao perfil &quot;[!UICONTROL Administrators]&quot; do produto para poder usar[!UICONTROL Control Panel](01:03 min)*

## Tutoriais do Painel de controle do Campaign

* **Gerenciamento de servidores SFTP**

   *Saiba como monitorar a capacidade do servidor, endereços IP de lista de permissões e adicionar chaves SSH:*

   * [Monitorar a capacidade do servidor, permitindo a listagem de endereços IP e a adição de chaves SSH](/help/administrating/control-panel/monitoring-server-capacity-allow-listing-adding-ssh-key.md)
   * [Gerar uma chave SSH](/help/administrating/control-panel/generate-ssh-key.md)
   * [Conectar um servidor SFTP](/help/administrating/control-panel/connect-to-sftp-server.md)
* **[Delegar subdomínios](/help/administrating/control-panel/subdomain-delegation.md)**

   *Saiba como delegar completamente um subdomínio ao Adobe Campaign*
* **[Adicionar certificados SSL](/help/administrating/control-panel/adding-ssl-certificates.md)**

   *Saiba como adicionar certificados SSL para proteger seus subdomínios.*

* **[Gerenciamento de registros TXT do Google](/help/administrating/control-panel/google-txt-record-management.md)**

   *Saiba como adicionar registro de verificação do site Google TXT a todos os seus subdomínios usados para enviar emails para endereços GMAIL por meio do Painel de controle do Campaign.*

* **Gerenciamento de chaves GPG**

   *Saiba como gerar e instalar um par de chaves públicas/privadas em uma instância do Campaign especificada para criptografar dados de saída, bem como importar e instalar uma chave pública em uma instância do Campaign para descriptografar dados de entrada:*

   * [Gerar e instalar chaves GPG para criptografia de dados](./gpg-key-management/generating-and-installing-gpg-keys-for-data-encryption.md)
   * [Usar uma chave GPG para criptografar dados](./gpg-key-management/using-a-gpg-key-to-encrypt-data.md)
   * [Descriptografia de dados](./gpg-key-management/decrypting-data.md)

* **[Solução de problemas](/help/administrating/control-panel/trouble-shooting.md)**

   *Saiba como solucionar problemas do Painel de controle do Campaign*

## Recursos adicionais

* [Centro de ajuda do Painel de controle do Campaign](https://docs.adobe.com/content/help/pt-BR/control-panel/using/control-panel-home.translate.html)

