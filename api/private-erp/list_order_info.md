# Listar Dados de Pedido

{% api-method method="get" host="https://api.gestao.plus" path="/order-external?t=:public_token" %}
{% api-method-summary %}
Listar Dados de Pedido
{% endapi-method-summary %}

{% api-method-description %}
Com esta rota você pode trazer os dados de um pedido.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="public_token" type="string" required=true %}
Token público do pedido
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}
Token de acesso ERP
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Informações do pedido listadas com sucesso.
{% endapi-method-response-example-description %}

```json
{
    "data": {
        "id": 593,
        "type": "V",
        "code": "0000593098",
        "date": {
            "date": "2021-03-02 21:02:53.000000",
            "timezone_type": 3,
            "timezone": "UTC"
        },
        "status": 1,
        "orderDiscount": 0,
        "orderTotal": 150,
        "statusPayment": "CONCLUIDO",
        "user": {
            "id": 2,
            "document": "123421341234",
            "name": "Solucoes Inteligentes Servicos EIRELI",
            "stateRegistration": null,
            "email": "example@example.com",
            "phone": null,
            "cellphone": "123423434",
            "state": "PB",
            "city": "Joao Pessoa",
            "address": "Avenida Dom Pedro ii",
            "neighborhood": "Centro",
            "number": 972,
            "addressDetail": "Sala 107",
            "zipCode": "1232343"
        },
        "orderItems": [
            {
                "id": 483,
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
        "financialItems": [
            {
                "id": 488,
                "code": "GOPAGHOM_708=============a",
                "dueDate": {
                    "date": "2021-03-02 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "UTC"
                },
                "installment": 1,
                "amountPaid": 75,
                "amount": 75,
                "type": "CARTAO_CREDITO",
                "status": "LIQUIDADO",
                "payment": []
            },
            {
                "id": 489,
                "code": "GOPAGHOM_708f=============0b954a",
                "dueDate": {
                    "date": "2021-04-01 00:00:00.000000",
                    "timezone_type": 3,
                    "timezone": "UTC"
                },
                "installment": 2,
                "amountPaid": 75,
                "amount": 75,
                "type": "CARTAO_CREDITO",
                "status": "LIQUIDADO",
                "payment": []
            }
        ],
        "attachmentItems": [
            {
                "id": 140,
                "description": "Hello world",
                "type": 0,
                "typeDescription": "Boleto",
                "name": "hello-world.pdf",
                "href": "https://dev.gestao.plus/file?forceDownload=false&q=e2dvb2RfbG9va317ImRhdGEiOnsidXVpZCI6IjUyMjhjOTNhLTdiYTAtMTFlYi1iMzNiLTAyNDJhYzExMDAwMyJ9LCJobWFjIjoiMmNiMzc1MjQ2NThjZjQ3Njg4NTA3OGVjYmIwYWFhMjJlYzE2YTA4OTVhNTY3NDU5NDM2NDFiMjJmNzhhNzZlZSIsIm5vbmNlIjoiNDQ2MDE2MjIwNjI2MzAifQ=="
            }
        ],
        "negotiationType": {
            "id": 22,
            "description": "E-commerce - Cartão de crédito 2x",
            "paymentSettings": {
                "paymentMethod": "CARTAO_CREDITO",
                "installments": 2
            },
            "installments": [
                {
                    "id": 38,
                    "paymentMethod": "CARTAO_CREDITO",
                    "generatePaymentBoleto": null,
                    "generatePaymentCreditCard": true,
                    "installmentDueDate": 0,
                    "installmentPercent": 50,
                    "installmentsType": 2,
                    "installments": 2,
                    "installment": 1
                },
                {
                    "id": 39,
                    "paymentMethod": "CARTAO_CREDITO",
                    "generatePaymentBoleto": null,
                    "generatePaymentCreditCard": true,
                    "installmentDueDate": 30,
                    "installmentPercent": 50,
                    "installmentsType": 2,
                    "installments": 2,
                    "installment": 2
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
Token de acesso ao pedido inválido.
{% endapi-method-response-example-description %}

```json
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (Invalid token)"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token do ERP inválido.
{% endapi-method-response-example-description %}

```json
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

