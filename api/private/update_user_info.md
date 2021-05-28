# Atualizar Dados do Usuário

{% api-method method="patch" host="https://api.gestao.plus" path="/user/:id" %}
{% api-method-summary %}
Atualizar informações do usuário
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que você atualize os dados de um determinado usuário, enviando os novos dados dentro do corpo da requisição.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
Origem da requisição.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authentication" type="string" required=true %}
Token de autenticação gerado durante o login
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="zipCode" type="string" required=true %}
CEP
{% endapi-method-parameter %}

{% api-method-parameter name="address" type="string" required=true %}
Novo endereço
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao alterar informações de usuário.
{% endapi-method-response-example-description %}

```text
{
    "address": "My new address",
    "zipCode": "74000000",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user/108"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Erro ao atualizar campo solicitado.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "You cannot change the field: fieldname"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Access Token Inválido.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

