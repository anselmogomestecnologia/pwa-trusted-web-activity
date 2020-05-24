

# Publicando seu PWA na Play Store usando Trusted Web Activity

O uso dos recursos deste respositório parte dos seguintes pressupostos:

1 - Você já tem o Android Studio 3.6.3 ou superior já instalado e funcional, com a SDK e o mínimo ncessário para usá-lo
2 - Sabe usar razoavelmente o Android Studio, não precisa ser um ninja
3 - Tem o Git instalado em seu computador para clonar o repositório
4 - Tem noções razoáveis de Java para editar os arquivos
5 - Tem um conta de desenvolvedor Android e acesso ao Google Play Console

[Transforme seu PWA em uma Trusted Web Activity](https://www.anselmo.com.br/blog/5/transforme-seu-pwa-em-uma-trusted-web-activity.html)

Escolha um diretório no seu computador e clone este repositório:

```
git clone https://github.com/anselmogomestecnologia/pwa-trusted-web-activity.git
```
Abra o Android Studio e importe o diretório clonado deste repositório.

Modifique os valoes dos URLs e das cores em `app/build.gradle` na pasta do projeto para apontar para o URL do seu PWA e personalizar as cores.

Para alterar os URLs, modifique os itens destacados:

        manifestPlaceholders = [
                hostName: "[URL RAIZ DO SITE ONDE ESTÁ SEU PWA]",
                defaultUrl: "[URL DE SEU PWA]",
                launcherName: "[TÍTULO/NOME DE SEU PWA]",
                assetStatements: '[{ "relation": ["delegate_permission/common.handle_all_urls"], ' + '"target": {"namespace": "web", "site": "[URL DE SEU PWA]"}}}]'
        ]
        
e altere também:

       hostName: "[URL RAIZ DO SITE ONDE ESTÁ SEU PWA]",
       defaultUrl: "[URL DE SEU PWA]",
       launcherName: "[TÍTULO/NOME DE SEU PWA]",
                
       assetStatements: '[{ "relation": ["delegate_permission/common.handle_all_urls"], ' +
       '"target": {"namespace": "web", "site": "[URL DE SEU PWA]"}}]'

Para modificar as cores, altere os itens a seguir:

        resValue "color", "colorPrimary", "#46008C"
        resValue "color", "colorPrimaryDark", "#46008C"
        resValue "color", "colorAccent", "#F78536"

Abra o projeto no Android Studio clique no botão Run. 

Repositórios de origem: 
https://github.com/GoogleChromeLabs/svgomg-twa.git
https://github.com/fireship-io/169-pwa-trusted-web-activity.git
