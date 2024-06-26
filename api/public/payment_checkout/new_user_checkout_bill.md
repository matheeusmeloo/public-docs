# Checkout de Novo Usuário \(Boleto\)

{% api-method method="post" host="https://api.gestao.plus" path="/order?t={token}" %}
{% api-method-summary %}
Checkout de novo usuário \(boleto\)
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que um novo usuário acesse o checkout com a forma de pagamento em boleto.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="t" type="string" required=true %}
Token para acesso ao checkout
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="items" type="string" required=true %}
Lista contendo os produtos comprados, cada um com 
{% endapi-method-parameter %}

{% api-method-parameter name="userData" type="string" required=true %}
Objeto contendo informações do usuário
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Tipo do pedido, neste caso "V" de venda
{% endapi-method-parameter %}

{% api-method-parameter name="negotiationType" type="string" required=true %}
ID da forma de pagamento escolhida \(boleto, cartão...\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao confirmar pedido no boleto.
{% endapi-method-response-example-description %}

```
{
   "code":"",
   "data":{
      "id":975, // ID DA VENDA
      "orderCode":"000097XYZ8" // CODIGO DA VENDA
   },
   "publicToken":"TOKEN PUBLICO DO PEDIDO",
   "type":"http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
   "title":"ok",
   "status":200,
   "detail":"Order created"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token de acesso inválido.
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

### Exemplo de Corpo da Requisição:

```text
{
    "negotiationType": "20",
    "type": "V",
    "userData": {
        "document": "123123123",
        "name": "João Diniz",
        "email": "example@example.com",
        "cellphone": "(62) 00000-0000",
        "zipCode": "12312-130",
        "address": "Avenida T 2",
        "number": "322",
        "neighborhood": "Setor A",
        "complement": "Apt 123123",
        "city": "Goiânia",
        "state": "GO"
    },
    "items": [
        {
            "id": "9",
            "quantity": 1
        }
    ]
}
```

