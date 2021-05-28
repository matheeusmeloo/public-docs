# Obter Produtos/Preços

{% api-method method="get" host="https://api.gestao.plus" path="/order/info?q=options&p=&t=prices" %}
{% api-method-summary %}
Listar produtos e seus preços
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint permite a listagem dos produtos e preços disponíveis.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
Query selecionada para consulta, neste caso queremos consultar os dados "data".
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="string" required=true %}
Não é necessário ser preenchido, porém precisa estar presente na requisição.
{% endapi-method-parameter %}

{% api-method-parameter name="t" type="string" required=true %}
Grupo de entidades sobre o qual a busca será feita, neste caso "company".
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar informações de produtos e preços.
{% endapi-method-response-example-description %}

```text
{
    "prices": [
        {
            "id": 9,
            "sku": "10",
            "description": "CERTIFICADO PJ A1",
            "status": 1,
            "price": 235,
            "image": {
                "name": "cert_soluti_a1_4_7.png",
                "description": "cert_soluti_a1_4_7.png",
                "href": "https://dev.gestao.plus/file?q={}=="
            },
            "groupDescription": "Certificado"
        },
        {
            "id": 10,
            "sku": "370",
            "description": "KIT PJ A3 - TOKEN - 2 ANOS",
            "status": 1,
            "price": 485,
            "image": {
                "name": "bradesco.png",
                "description": "bradesco.png",
                "href": "https://dev.gestao.plus/file?q={}=="
            },
            "groupDescription": "Servicos"
        }
        .
        .
        .
    ],
    "image": [],
    "description": "Unidade - GOIOERÊ",
    "origin": "VENDA_ONLINE",
    "id": null,
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/order/info"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token de acesso inválido
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (Invalid token)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

