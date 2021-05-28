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

