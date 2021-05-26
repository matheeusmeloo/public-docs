# Listar Contatos \(Dados Bancários\)

{% api-method method="get" host="https://api.gestao.plus" path="/user-contact" %}
{% api-method-summary %}
Listar contatos
{% endapi-method-summary %}

{% api-method-description %}
Você pode listar as contas bancárias adicionadas ao parceiro através desta rota.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Autenticação modelo \(Bearer {token}\)
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar contatos
{% endapi-method-response-example-description %}

```
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-contact"
        }
    },
    "_embedded": {
        "user_contact": []
    },
    "total_items": 0
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Acesso não autorizado.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



