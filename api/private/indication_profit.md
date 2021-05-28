# Listar Ganho por Indicação

{% api-method method="get" host="https://api.gestao.plus" path="/user-indication-gain" %}
{% api-method-summary %}
Listar os ganhos em indicações.
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode listar os seus ganhos de indicação em cada produto
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token modelo "Bearer {token}"
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar ganhos por indicação
{% endapi-method-response-example-description %}

```text
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-indication-gain"
        }
    },
    "_embedded": {
        "user_indication_gain": []
    },
    "total_items": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Access Token Inválido
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

