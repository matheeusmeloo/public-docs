# Checkout \(Cartão de Crédito\)

{% api-method method="patch" host="https://api.gestao.plus" path="/order/info?q=options&p=&t=prices" %}
{% api-method-summary %}
Checkout de pagamento para cartão de crédito
{% endapi-method-summary %}

{% api-method-description %}
Com este endpoint você pode alterar as informações do cartão de crédito utilizado no checkout.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
Parametro de consulta, neste caso utilizaremos "options".
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="string" required=true %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="t" type="string" required=true %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="cardData" type="string" required=true %}
Um objeto contendo os dados do cartão, seu nome "holderName", o mês de expiração "expirationMonth", ano de expiração "expirationYear", código de segurança "securityCode" e número do cartão "cardNumber".
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao alterar os dados do cartão.
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
    "detail": "Fail to start checkout, payment cannot executed when status = 'CONCLUIDO'"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://api.gestao.plus" path="/order/info?q=options&p=&t=prices" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

