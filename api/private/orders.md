# Pedidos \(Compras\)

{% api-method method="get" host="https://api.gestao.plus" path="/order" %}
{% api-method-summary %}
Listar Pedidos
{% endapi-method-summary %}

{% api-method-description %}
Através desta rota você pode listar os seus pedidos.
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar pedidos.
{% endapi-method-response-example-description %}

```text
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/order"
        }
    },
    "_embedded": {
        "order": [
            {
                "id": 430,
                "type": "V",
                "code": "123123123",
                "date": {
                    "date": "2021-01-27 16:59:34.000000",
                    "timezone_type": 3,
                    "timezone": "UTC"
                },
                "status": 0,
                "orderDiscount": "0.00",
                "orderTotal": "0.00",
                "statusPayment": null,
                "_links": {
                    "self": {
                        "href": "https://api.gestao.plus/order/430"
                    }
                }
            },
            {
                "id": 884,
                "type": "V",
                "code": "123123123",
                "date": {
                    "date": "2021-05-07 19:38:04.000000",
                    "timezone_type": 3,
                    "timezone": "UTC"
                },
                "status": 1,
                "orderDiscount": "0.00",
                "orderTotal": "395.00",
                "statusPayment": "PENDENTE",
                "_links": {
                    "self": {
                        "href": "https://api.gestao.plus/order/884"
                    }
                }
            }
        ]
    },
    "total_items": 11
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Sem permissão para listar os pedidos.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

