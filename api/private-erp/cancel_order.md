# Cancelar Pedido

{% api-method method="delete" host="https://api.gestao.plus" path="/order-external/:orderId" %}
{% api-method-summary %}
Cancelar Pedido
{% endapi-method-summary %}

{% api-method-description %}
Com esta rota você pode cancelar um pedido.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="orderId" type="string" required=true %}
ID do pedido
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}
Token de acesso ERP
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Pedido cancelado com sucesso.
{% endapi-method-response-example-description %}

```json
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unknown",
    "status": 200,
    "detail": "Venda/movimentação cancelada com sucesso"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token de acesso ao pedido inválido.
{% endapi-method-response-example-description %}

```json
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (Invalid token)"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token do ERP inválido.
{% endapi-method-response-example-description %}

```json
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden, invalid key (x-api-key)"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Pedido não encontrado.
{% endapi-method-response-example-description %}

```json
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Not Found",
    "status": 404,
    "detail": "Order not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}