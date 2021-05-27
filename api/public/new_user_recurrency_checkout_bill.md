# Checkout de Recorrência em Novo Usuário \(Boleto\)

{% api-method method="post" host="https://api.gestao.plus" path="/order?t={token}" %}
{% api-method-summary %}
Checkout de recorrência para novo usuário pagando em boleto
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite que você acesse o checkout de pagamentos como um novo usuário pagando em boleto.
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
Token de acesso para o checkout
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="items" type="string" required=true %}
Lista com os itens selecionados para o checkout,   
cada um com o seu id e quantidade.
{% endapi-method-parameter %}

{% api-method-parameter name="userData" type="string" required=true %}
Objeto com os dados do usuário, seu email, nome, endereço...
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Tipo de pedido, neste caso "R" de recorrência.
{% endapi-method-parameter %}

{% api-method-parameter name="negotiationType" type="string" required=true %}
ID do tipo de negociação usado \(boleto, cartão...\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao carregar checkout.
{% endapi-method-response-example-description %}

```

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



