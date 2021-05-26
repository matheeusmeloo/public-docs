# Opções de Pagamento no Indicador

{% api-method method="get" host="https://api.gestao.plus" path="/order/info?q=options&p=i1\_goiere&t=negotiationTypes" %}
{% api-method-summary %}
Listar opções de pagamento por indicador
{% endapi-method-summary %}

{% api-method-description %}
Liste as formas de recebimento do parceiro indicador com esta rota.  
A diferença desta rota para a listagem na unidade é o "i" no parâmetro "p".
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="p" type="string" required=true %}
A unidade da qual iremos filtrar os tipos de negociação utilizados, aqui utilizamos "u4\_goiere"
{% endapi-method-parameter %}

{% api-method-parameter name="t" type="string" required=true %}
A informação que queremos sobre o parametro "p", nessa consulta escolhemos a "negotiationTypes", para listar as formas de recebimento desta unidade.
{% endapi-method-parameter %}

{% api-method-parameter name="q" type="boolean" required=true %}
A consulta "query" a ser realizada sobre os pedidos, neste caso iremos utilizar "options".
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar as formas de recebimento do indicador.
{% endapi-method-response-example-description %}

```
{
    "negotiationTypes": [
        {
            "id": 8,
            "description": "Boleto",
            "paymentSettings": {
                "paymentMethod": "BOLETO",
                "installments": 0
            }
        },
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
        },
        {
            "id": 23,
            "description": "E-commerce - Cartão de crédito 3x",
            "paymentSettings": {
                "paymentMethod": "CARTAO_CREDITO",
                "installments": 3
            }
        }
    ],
    "image": {
        "name": "data_imgntG2Pi",
        "description": null,
        "href": "https://dev.gestao.plus/file?q={}=="
    },
    "description": "Outro texto contabilidade",
    "origin": "VENDA_ONLINE_INDICADOR",
    "id": "1",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/order/1"
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

