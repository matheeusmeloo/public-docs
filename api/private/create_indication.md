# Criar Indicação

{% api-method method="post" host="https://api.gestao.plus" path="/user-indication" %}
{% api-method-summary %}
Criar Indicação
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode criar indicações.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Autenticação no modelo "Bearer Token"
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Email do indicado
{% endapi-method-parameter %}

{% api-method-parameter name="cellphone" type="string" required=true %}
Celular
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}
Telefone do Indicado
{% endapi-method-parameter %}

{% api-method-parameter name="document" type="string" required=true %}
CPF ou CNPJ
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Nome do indicado
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Sucesso ao criar indicação.
{% endapi-method-response-example-description %}

```
{
    "name": "GESTAO ONLINE E SOLUCOES EM SOFTWARE LTDA",
    "document": "123123123112",
    "phone": "12312312312",
    "cellphone": "12312312312",
    "email": "email@gestao.plus",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-indication"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
O usuário que deseja indicar já foi indicado por outra pessoa.
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "The user is already indicated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



