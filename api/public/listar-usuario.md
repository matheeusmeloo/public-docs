# Informações do Usuário

{% api-method method="post" host="https://api.gestao.plus" path="/user?q=info" %}
{% api-method-summary %}
Listar Usuário
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota podemos listar as informações de um usuário em específico.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
"application/json"
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" %}
"info"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Corpo da requisição inválido.
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "Invalid e-mail, value is empty"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=422 %}
{% api-method-response-example-description %}
Email inválido.
{% endapi-method-response-example-description %}

```
{
    "reason": "1",
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unprocessable Entity",
    "status": 422,
    "detail": "You cannot use this email"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



