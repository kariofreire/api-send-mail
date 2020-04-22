<div align="center">
  <img src="assets/images/icon-message.png" width="100px">
  <hr width="48px">
</div>

### :rocket: EXEMPLO DE USO
#
Enviar Email usando servidor da 000WebHost.
A Hosting oferece uma quota de 50 envio de emails diários por cada conta. Criei esse modelo de API para ajudar os demais interessados já que muitos não tem suporte de envios de email em seu servidor ou aplicação.
Para isso é super simples, você vai precisar da CDN jQuery.

Segue a url do arquivo hospedado em nosso projeto:
```
https://apimailkariofreire.000webhostapp.com//view/assets/js/bootstrap.min.js
```

Segue agora um modelo de como estar enviando email com API.

Os parâmetros passados são **(user_name, user_mail_for, user_message)**
```
$.post("https://apimailkariofreire.000webhostapp.com/controller/api.php", {
  user_name: "kariofreire",
  user_mail_for: "kariofreire@gmail.com",
  user_message: "Olá, estou enviando essa mensagem pela API MAIL KFTECH"
}, function(result) {
  console.log(result);
});
```
O valor retornado é por código onde:

- 0 (Falha ao enviar)
- 1 (Enviado com sucesso)
- 2 (Quota diária completa)

Para consultar a Quota diária é simples, segue abaixo um exemplo:

```
$.post("https://apimailkariofreire.000webhostapp.com/controller/count-quota.php", function(result) {
  console.log(result);
});
```

Segue abaixo um modelo de retorno da Request:

```
E-mails enviados hoje: **X**.
```

###### (Onde **X** é a quantidade de emails enviados no dia)
---
Feito com ❤️ by Kário Freire
