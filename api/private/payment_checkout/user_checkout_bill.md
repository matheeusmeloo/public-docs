# Checkout Usuário \(Boleto\)

{% api-method method="post" host="https://api.gestao.plus" path="/order" %}
{% api-method-summary %}
Checkout do usuário no boleto
{% endapi-method-summary %}

{% api-method-description %}
Com esta rota você pode gerar pedidos de um determinado produto.
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
Um array contendo objetos com o id do produto e quantidade comprada
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Tipo da movimentação, geralmente "V" de venda
{% endapi-method-parameter %}

{% api-method-parameter name="negotiationType" type="string" required=true %}
Tipo de negociação utilizado para a compra
{% endapi-method-parameter %}

{% api-method-parameter name="uri" type="string" required=true %}
Identificador do cliente
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao gerar pedido.
{% endapi-method-response-example-description %}

```text
{
   "code":"",
   "data": {
      "id":954,
      "orderCode": "0000954179"
   },
   "publicToken":"OOTU0_MTYyMjIyMTMzMzMwMTU_qOJpy605WkWxYaAhEhF76w",
   "type":"http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
   "title":"ok",
   "status":200,
   "detail":"Order created"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Requisição inválida
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

