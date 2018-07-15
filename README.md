# # Ambari Custom Service for Streamsets

[![N|Solid](https://19ttqs47cfw33zkecq3dz58m-wpengine.netdna-ssl.com/wp-content/uploads/2015/08/small_logo_2.png)](https://nodesource.com/products/nsolid)

Guia de apoio para instalar e gerênciar um serviço customizado para o Streamsets. A plataforma StreamSets DataOps simplifica a forma de construir, executar, operar e proteger arquiteturas de movimentação de dados corporativos.

### Observações

  - Ambari devidamente instalado e executando.
  - Nenhuma prévia instalação do Streamsets.

    Siga os passos para instalar e gerênciar o Streamsets pelo Ambari.

# Implantando Stremsets no HDP 2.6
    
    cd /var/lib/ambari-server/resources/stacks/HDP/2.6/services
    mkdir STREAMSETS
    git clone https://github.com/tharcisiofernand/Ambari-Streamsets.git

# Reiniciando o Ambari

    systemctl stop ambari-server
    systemctl stop ambari-agent
    
    systemctl start ambari-agent
    systemctl start ambari-server

# Adicionando o serviço

  - Em seguida, você pode clicar em 'Adicionar serviço' no menu suspenso 'Ações' no canto inferior esquerdo do painel do Ambari:
  - No canto inferior esquerdo -> Ações -> Adicionar serviço -> marque Streamsets -> Next ->
  - ### Imagem

  - Selecione em qual host deseja instalar o serviço -> Next
  - ### Imagem
  
  - Nesta tela podemos alterar o arquivos de configurações dos Streamsets ('sdc.properties') e as variáveis de ambientes -> Next
  - ![](../properties.png)


  - Por fim clique em implantar o serviço -> Deploy
  - ### Imagem
  

  - Ao final receberemos uma mensagem de instalação bem sucessida, a partir deste ponto temos o gerênciamento do Streamsets de forma mais prática através do Ambari, podendo iniciar, parar e configurar seu serviço.
  - ### Imagem

# Gerênciamento
  - Clicando sobre o componente Streamsets é possível visualizar a aba "Configs", onde podemos alterar as configurações do componente.
  - ### Imagem

