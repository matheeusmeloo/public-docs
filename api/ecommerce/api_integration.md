---
description: A URL é montada em forma de array com parâmetros determinados.
---

# Integração API

{% api-method method="get" host="https://tools.gestao.plus" path="/goto-checkout.php" %}
{% api-method-summary %}
URL Checkout
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite que você gere uma URL para acessar o checkout com os devidos parâmetros.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Accept" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="user" type="string" required=true %}
Dados do usuário para o preenchimento automático do formulário \(Opcional\)
{% endapi-method-parameter %}

{% api-method-parameter name="sku" type="string" required=true %}
SKU do produto dessa venda
{% endapi-method-parameter %}

{% api-method-parameter name="callBackUrl" type="string" required=true %}
URL de volta para o usuário retornar, se for necessário \(Opcional\)
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="string" required=true %}
ID gerado dentro do sistema \(Opcional, consulte o administrador\)
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=true %}
URL do ERP Gestão Online
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao requisitar url do checkout.
{% endapi-method-response-example-description %}

```
{
    "status": "success",
    "redirectTo":
    "https://dev.gestao.plus/loja/checkout?p=i1-contabilidade-indicador&loc
    k=1&item=eyJyYW5kIjoxLCJza3UiOjEwfQ%3D%3D&payload=eyJkb2
    N1bWVudCI6IjExMTExMTExMTExIiwibmFtZSI6Ik5vbWUgRXhlbXBsb
    yIsImVtYWlsIjoidGVzdGVAdGVzdGUuY29tIiwiY2VsbHBob25lIjoiNjI5O
    TU1NTU1NTUiLCJ6aXBDb2RlIjoiNzQyMzAxMzAiLCJhZGRyZXNzIjoi
    QXB0IDEyMyIsIm51bWJlciI6IjE1MjkiLCJuZWlnaGJvcmhvb2QiOiJTZX
    RvciBCdWVubyIsImFkZHJlc3NEZXRhaWwiOiJBdiBYcHRvIiwiY2l0eSI
    6IkdvaWFuaWEiLCJzdGF0ZSI6IkdPIn0%3D&callBackUrl=https%3A%
    2F%2Fseusiteintegrado.com.br%2Fexemplo%2F123"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Corpo da requisição inválido.
{% endapi-method-response-example-description %}

```
{
    "status": "error",
    "message": "An error occurred, the 'url' parameter is invalid"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



