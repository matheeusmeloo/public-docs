# Checkout de Novo Usuário \(Cartão de Crédito\)

{% api-method method="post" host="https://api.gestao.plus" path="/order?t={token}" %}
{% api-method-summary %}
Checkout para acesso de novo usuário pagando em cartão de crédito
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que um novo usuário acesse o checkout com o cartão de crédito como forma de pagamento.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="t" type="string" required=true %}
Token para acesso ao checkout.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao confimar venda como novo usuário.
{% endapi-method-response-example-description %}

```
{
   "code":"",
   "data":{
      "id":978,
      "orderCode":"0000978172" // CÓDIGO DO PEDIDO
   },
   "publicToken":"TOKEN PÚBLICO DA VENDA",
   "type":"http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
   "title":"ok",
   "status":200,
   "detail":"Order created"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token de acesso inválido
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (Invalid token)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Exemplo do Corpo da Requisição.

```text
{
    "uri": "u4_contador-indicador",
    "negotiationType": "23",
    "type": "V",
    "userData": {
        "document": "7187382837",
        "name": "João Diniz",
        "email": "example@exemple.com",
        "cellphone": "(62) 123123-123",
        "zipCode": "123123-23",
        "address": "Avenida T 14",
        "number": "1111",
        "neighborhood": "Setor A",
        "complement": "Apt 123",
        "city": "Goiânia",
        "state": "GO"
    },
    "cardData": {
        "holderName":"VISA MAGIC",
        "expirationMonth":"05",
        "expirationYear":"2021",
        "securityCode":"123",
        "cardNumber":"4539003871725497"
    },
    "items": [
        {
            "id": "9",
            "quantity": 1
        }
    ]
}
```

