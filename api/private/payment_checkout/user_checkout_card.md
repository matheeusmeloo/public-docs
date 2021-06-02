# Checkout Usuário \(Cartão de Crédito\)

{% api-method method="post" host="https://api.gestao.plus" path="/order" %}
{% api-method-summary %}
Checkout de usuário \(Cartão de Crédito\)
{% endapi-method-summary %}

{% api-method-description %}
Rota para criação de pedido em cartão de crédito.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token no modelo "Bearer {token}"
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="items" type="string" required=true %}
Lista contendo objetos com ID e quantidade de cada produto comprado.
{% endapi-method-parameter %}

{% api-method-parameter name="cardData" type="string" required=true %}
Informações do cartão de crédito, um objeto  
contendo, holderName \(bandeira do cartão\),  
expirationMonth \(mês de expiração\), expirationYear \(ano de expiração\), securityCode \(código de segurança\), cardNumber \(número do cartão\).
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Tipo do pedido, geralmente "V" de venda
{% endapi-method-parameter %}

{% api-method-parameter name="negotiationType" type="string" required=true %}
ID do tipo de negociação utilizado para o pedido
{% endapi-method-parameter %}

{% api-method-parameter name="uri" type="string" required=true %}
Identificador do cliente
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao criar pedido.
{% endapi-method-response-example-description %}

```text
{
   "code":"",
   "data":{
      "id":968,
      "orderCode":"0000968179" // Numero do pedido
   },
   "publicToken":"TOKEN PÚBLICO",
   "type":"http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
   "title":"ok",
   "status":200,
   "detail":"Order created"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Requisição inválida.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "Invalid negotiation type for this scope"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Exemplo do corpo da requisição:

```text
{
   "uri":"",
   "type":"V",
   "negotiationType":21,
   "items":[
      {
         "id":9,
         "sku":"10",
         "p":"",
         "quantity":1,
         "price":235,
         "description":"CERTIFICADO PJ A1",
         "image":{
            "name":"cert_soluti_a1_4_7.png",
            "description":"cert_soluti_a1_4_7.png",
            "href":"https://dev.gestao.plus/file?q={imagedata}=="
         },
         "rand":"3123123123"
      }
   ],
   "userData":{
      "document":"283823819230",
      "name":"Kallebe Gomes Bezerra",
      "email":"kallebe3123123@gmail.com",
      "cellphone":"(62) 9323-2312",
      "zipCode":"74000-000",
      "address":"My new address",
      "number":0,
      "neighborhood":"Residencial Alphaville Flamboyant",
      "addressDetail":"...",
      "city":"Goiânia",
      "state":"GO",
      "password":null,
      "phone":"",
      "username":"3232323213"
   },
   "cardData":{
      "holderName":"Kallebe Gomes",
      "expirationMonth":"5",
      "expirationYear":"2021",
      "securityCode":"123",
      "cardNumber":"4539003370725497"
   }
}
```

