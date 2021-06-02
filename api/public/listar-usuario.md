# Informações do Usuário

{% api-method method="post" host="https://api.gestao.plus" path="/user?q=info" %}
{% api-method-summary %}
Informações de um usuário
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite que você busque por informações de um usuário em específico através de seu CPF, caso ele já tenha sido registrado as suas informações serão retornadas.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
info
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="document" type="string" required=true %}
CPF do usuário
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao buscar por usuário
{% endapi-method-response-example-description %}

```
{
    "haveAccount": true,
    "havePassword": true,
    "allowGuest": true,
    "data": {
        "email": "paulo.******@live.com",
        "cellphone": "6299183****",
        "guestUserToken": "TOKEN QUE SERÁ USADO PARA REALIZAR OS PEDIDOS" // IMPORTANTE
    },
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Erro ao buscar por usuário
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "Invalid document"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



