# Listar Dados do Usuário

{% api-method method="get" host="https://api.gestao.plus" path="/user?filter\[0\]\[field\]=id&filter\[0\]\[type\]=eq&filter\[0\]\[value\]=$USER\_ID" %}
{% api-method-summary %}
Listar informações de um usuário
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você conseguirá listar as informações de um usuário.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Bearer {Seu TOKEN}
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="filter\[0\]\[value\]" type="string" required=true %}
$USER\_ID
{% endapi-method-parameter %}

{% api-method-parameter name="filter\[0\]\[field\]" type="string" required=true %}
id
{% endapi-method-parameter %}

{% api-method-parameter name="filter\[0\]\[type\]" type="string" required=true %}
eq
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar informações do usuário.
{% endapi-method-response-example-description %}

```text
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user"
        }
    },
    "_embedded": {
        "user": [
            {
                "id": 5510,
                "username": "SEU NOME DE USUÁRIO",
                "document": "SEU DOCUMENTO CPF/CNPJ",
                "name": "NOME",
                "email": "EMAIL",
                "phone": "SEU TELEFONE",
                "cellphone": "SEU CELULAR",
                "businessPhone": null,
                "zipCode": "SEU CEP",
                "address": "Rua Bela Vista",
                "number": 0,
                "addressDetail": null,
                "neighborhood": "Centro",
                "city": "cidade",
                "state": "estado",
                "dateCreated": {
                    "date": "2021-02-04 15:51:17.000000",
                    "timezone_type": 3,
                    "timezone": "UTC"
                },
                "_links": {
                    "self": {
                        "href": "https://api.gestao.plus/user/5510"
                    }
                }
            }
        ]
    },
    "total_items": 1
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Token de acesso inválido.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

