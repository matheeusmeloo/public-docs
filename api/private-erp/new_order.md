# Criar Pedido

{% api-method method="post" host="https://api.gestao.plus" path="/order-external" %}
{% api-method-summary %}
Criar um novo pedido
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode adicionar um contato ao usuário.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}
Token de acesso ERP
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="code" type="string" required=false %}
Código de identificação da venda
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="string" required=false %}
Data da venda: Y-m-d H:i:s 
{% endapi-method-parameter %}

{% api-method-parameter name="note" type="string" required=false %}
Observação
{% endapi-method-parameter %}

{% api-method-parameter name="user" type="object" required=true %}
{% api-method-parameter name="name" type="string" required=true %}
Nome
{% endapi-method-parameter %}
{% api-method-parameter name="nameLaw" type="string" required=true %}
Razão Social
{% endapi-method-parameter %}
{% api-method-parameter name="email" type="string" required=true %}
E-mail
{% endapi-method-parameter %}
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="array" required=true %}
Objeto com os dados dos itens
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Criação do pedido com sucesso.
{% endapi-method-response-example-description %}

```text
{
    "code": "SUCCESS_ORDER_CREATED",
    "data": {
        "publicToken": "OMzMyMQ_MTY4OTYyMjM4MDUEaa1xNjE_7C44FWNkaVR-GJB871Mb2g",
        "orderCode": "CÓDIGO_DA_VENDA_GERADA"
    },
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unknown",
    "status": 201,
    "detail": "ok"
}

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token do ERP inválido.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden, invalid key (x-api-key)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Exemplo de corpo da requisição:

```text
{
    "code": "",
    "date": "",
    "note": "",
    "user": {
        "name": "",
        "nameLaw": "",
        "email": "",
        "document": "",
        "cellphone": "",
        "phone": "",
        "stateRegistration": "",
        "zipCode": "",
        "address": "",
        "number": "",
        "neighborhood": "",
        "addressDetail": "",
        "city": "",
        "state": ""
    },
    "orderItems": [
        {
            "product": "",
            "quantity": "",
            "price": "",
            "discount": ""
        }
    ]
}
```