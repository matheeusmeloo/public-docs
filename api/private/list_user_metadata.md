# Listar Metadados do Usuário

{% api-method method="get" host="https://api.gestao.plus" path="/user-metadata" %}
{% api-method-summary %}
Listar Metadados do Usuário
{% endapi-method-summary %}

{% api-method-description %}
Com essa rota você pode listar os metadados do usuário, como sua imagem de perfil.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
Origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Seu token de acesso
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="filter\[0\]\[value\]" type="string" required=false %}
"picture"
{% endapi-method-parameter %}

{% api-method-parameter name="filter\[0\]\[field\]" type="string" %}
"dataKey"
{% endapi-method-parameter %}

{% api-method-parameter name="filter\[0\]\[type\]" type="boolean" %}
"eq"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar metadados do usuário.
{% endapi-method-response-example-description %}

```
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-metadata"
        }
    },
    "_embedded": {
        "user_metadata": []
    },
    "total_items": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Token de acesso inválido.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



