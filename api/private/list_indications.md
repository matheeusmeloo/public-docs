# Listar Indicações

{% api-method method="get" host="https://api.gestao.plus" path="/user-indication" %}
{% api-method-summary %}
Listar Indicações
{% endapi-method-summary %}

{% api-method-description %}
Rota responsável pela listagem de indicados.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token no modelo "Bearer {Token}"
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar indicações
{% endapi-method-response-example-description %}

```
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-indication"
        }
    },
    "_embedded": {
        "user_indication": [
            {
                "id": 4,
                "document": "12312312312",
                "name": "Softwares e Solucoes",
                "email": "email@gestao.plus",
                "phone": null,
                "cellphone": "12312312312",
                "_links": {
                    "self": {
                        "href": "https://api.gestao.plus/user-indication/4"
                    }
                }
            },
            {
                "id": 666,
                "document": "123123123123",
                "name": "Conta Rapida",
                "email": "email@teste.com.br",
                "phone": "(81) 13123123123",
                "cellphone": null,
                "_links": {
                    "self": {
                        "href": "https://api.gestao.plus/user-indication/19"
                    }
                }
            }
        ]
    },
    "total_items": 3
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Access Token inválido.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



