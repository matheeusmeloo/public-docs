---
description: Listar as formas de pagamento disponíveis em uma determinada unidade.
---

# Opções de Pagamento na Unidade

{% api-method method="get" host="https://api.gestao.plus" path="/order/info?q=options&p=u4\_goiere&t=negotiationTypes" %}
{% api-method-summary %}
Formas de pagamento de uma unidade
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite a você listar as formas de pagamento de uma determinada unidade.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="t" type="string" required=true %}
A informação que queremos sobre o parametro "p",  
nessa consulta escolhemos a "negotiationTypes", para  
listar as formas de recebimento desta unidade.
{% endapi-method-parameter %}

{% api-method-parameter name="q" type="string" required=true %}
A consulta "query" a ser realizada sobre os pedidos, neste caso iremos utilizar "options".
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="boolean" required=true %}
A unidade da qual iremos filtrar os tipos de   
negociação utilizados, aqui utilizamos "u4\_goiere"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar as informações da unidade.
{% endapi-method-response-example-description %}

```
{
    "negotiationTypes": [
        {
            "id": 21,
            "description": "E-commerce - Cartão de crédito 1x",
            "paymentSettings": {
                "paymentMethod": "CARTAO_CREDITO",
                "installments": 1
            }
        },
        {
            "id": 22,
            "description": "E-commerce - Cartão de crédito 2x",
            "paymentSettings": {
                "paymentMethod": "CARTAO_CREDITO",
                "installments": 2
            }
        }
    ],
    "image": {
        "name": "airtonsena.jpg",
        "description": null,
        "href": "https://dev.gestao.plus/file?q={}=="
    },
    "description": "Unidade - Anapolis",
    "origin": "VENDA_ONLINE_UNIDADE",
    "id": "4",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/order/4"
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



