# Instagram Embed Discord Bot

>![Visitor Count](https://camo.githubusercontent.com/b69e969500158d8cef615ee33731cad5633144db5a13ba089fa5f9c102146d29/68747470733a2f2f6b6f6d617265762e636f6d2f67687076632f3f757365726e616d653d76656e61787974)<br>

Entrega novas postagens de contas do Instagram para um canal Discord.
Embed vídeos e imagens vinculados de usuários vinculados a postagens, vídeos e bobinas do Instagram em um bate-papo do Discord. O bot público tinha mais de 500 mil usuários em mais de 2 mil servidores antes de ser desligado pelo proprietário devido a restrições de recursos.

[Support Discord Server](https://discord.gg/TEMauza)

If you are here, please leave a ⭐️ at 

## Características:
- Sem prefixos necessários
- Os vídeos podem ser baixados
- Tamanhos de upload ajustados para servidores Nitro Boosted
- Suporta comandos de barra do Discord
- Suporta a assinatura de novas postagens de usuários do Instagram
- Várias contas IG para failover

## Exemplo: 
![Example of reels bot on discord](/docs/Content/ReadMe/Example.png)

### Como configurar:
Crie um novo arquivo chamado `config.json`, copie e cole o conteúdo abaixo nele, preencha-o e salve-o no mesmo diretório do arquivo executável do Instagram Embed. Substitua quaisquer campos opcionais e não preenchidos por `""`. Exemplo: `"OTPSecret": "",`. Se você receber um erro com sua formatação JSON, poderá verificar sua sintaxe JSON em [jsonlint.com](https://jsonlint.com/).
```
{
  "Token": "Token",
  "Prefix": [ "https://www.instagram.com/", "https://instagram.com/", "http://www.instagram.com/", "http://instagram.com/" ],
  "OwnerID": "ID",
  "TestGuildID": "ID",
  "DMErrors": true/false,

  "IGAccounts": [
    {
      "username": "IG Username",
      "password": "IG Password",
      "OTPSecret": "IG OTP Secret (optional)",
      "UsageTimes": [
        {
          "StartHour": optional (int; 0-23),
          "EndHour": optional (int; 0-23)
        }
      ]
    }
  ],

  "ProxyURL": "",
  "ProxyUsername": "username (optional)",
  "ProxyPassword": "password (optional)",

  "DisableTitle": false,

  "AllowSubscriptions": true/false,
  "MongoDBUrl": "MongoDB Connection String (Required for subscriptions)",
  "DefaultSubscriptionsPerGuildMax": 1,
  "HoursToCheckForNewContent": 3
}
```
