# Detalhes do Pedido

{% api-method method="get" host="https://api.gestao.plus" path="/order/:id" %}
{% api-method-summary %}
Detalhes do Pedido
{% endapi-method-summary %}

{% api-method-description %}
Listar detalhes de um pedido em específico.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID do pedido
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Access token no modelo "Bearer {token}"
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar os detalhes de um pedido.
{% endapi-method-response-example-description %}

```text
{
    "data": {
        "id": 430,
        "type": "V",
        "code": "123123123",
        "date": {
            "date": "2021-01-27 16:59:34.000000",
            "timezone_type": 3,
            "timezone": "UTC"
        },
        "status": 0,
        "orderDiscount": null,
        "orderTotal": null,
        "statusPayment": null,
        "user": {
            "id": 108,
            "document": "123123123123",
            "name": "Nome Usuario",
            "stateRegistration": null,
            "email": "email@gmail.com",
            "phone": "",
            "cellphone": "1231231231",
            "state": "GO",
            "city": "Goiânia",
            "address": "My new address",
            "neighborhood": "Residencial Alphaville",
            "number": 0,
            "addressDetail": "...",
            "zipCode": "74000000"
        },
        "orderItems": [
            {
                "id": 393,
                "quantity": 1,
                "price": 150,
                "description": "CERTIFICADO PJ A1",
                "image": {
                    "name": "cert_soluti_a1_4_7.png",
                    "description": "cert_soluti_a1_4_7.png",
                    "href": "https://dev.gestao.plus/file?q={}=="
                }
            }
        ],
        "financialItems": [],
        "attachmentItems": [],
        "negotiationType": {
            "id": 6,
            "description": "Dinheiro",
            "paymentSettings": {
                "paymentMethod": null,
                "installments": 0
            },
            "installments": [
                {
                    "id": 6,
                    "paymentMethod": null,
                    "generatePaymentBoleto": null,
                    "generatePaymentCreditCard": null,
                    "installmentDueDate": 0,
                    "installmentPercent": 100,
                    "installmentsType": null,
                    "installments": 0,
                    "installment": 0
                }
            ]
        }
    },
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unknown",
    "status": 200,
    "detail": "ok"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Você não pode ver os detalhes do pedido de outra pessoa além do acesso provido pelo seu Token.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

