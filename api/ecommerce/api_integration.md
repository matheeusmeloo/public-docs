---
description: A URL é montada em forma de array com parâmetros determinados.
---

# Integração API

{% api-method method="post" host="https://tools.gestao.plus" path="/goto-checkout.php" %}
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
{% api-method-parameter name="user" type="string" required=false %}
Dados do usuário para o preenchimento automático do formulário
{% endapi-method-parameter %}

{% api-method-parameter name="sku" type="string" required=true %}
SKU do produto dessa venda
{% endapi-method-parameter %}

{% api-method-parameter name="callBackUrl" type="string" required=false %}
URL de volta para o usuário retornar para o carrinho, se for necessário
{% endapi-method-parameter %}

{% api-method-parameter name="callBackResponseUrl" type="string" required=false %}
URL de volta para o usuário retornar para resumo de compra após a confirmação do pagamento, se for necessário \(a url deve esperar a concatenação do parâmetro de código do pedido\)
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="string" required=false %}
ID gerado dentro do sistema \(consulte o administrador\)
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

```text
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

```text
{
    "status": "error",
    "message": "An error occurred, the 'url' parameter is invalid"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


Exemplo de request:
```
curl --location --request POST 'https://tools.gestao.plus/goto-checkout.php' \
--header 'Content-Type: application/json' \
--data-raw '{
    "url": "https://parceirosoluti.com.br",
    "p": "i6473-gestao-online",
    "callBackUrl": "https://gestão.online?q=callbackToProductListSample",
    "callBackResponseUrl": "https://gestão.online?q=callbackToOrderDetailUsingCode&code=",
    "sku": 9,
    "user": {
        "document": "11111111111",
        "name": "Nome Exemplo",
        "email": "teste@teste.com",
        "cellphone": "62995555555",
        "zipCode": "74230130",
        "address": "Apt 123",
        "number": "1529",
        "neighborhood": "Setor Bueno",
        "addressDetail": "Av Xpto",
        "city": "Goiania",
        "state": "GO"
    }
}'
```


{% hint style="info" %}
Para consultar as informações utilize o código retornado na url indicada em "callBackResponseUrl", [utilize o endpoint de detalhes do pedido/pagamento](https://docs.gestao.plus/api/public/order_details_public) para obter os detalhes.
{% endhint %}

