# Detalhes da Empresa pelo Token

{% api-method method="get" host="https://api.gestao.plus" path="/order/info?q=data&p=&t=company" %}
{% api-method-summary %}
Listar detalhes da empresa através do token
{% endapi-method-summary %}

{% api-method-description %}
Este endpoint fornece as informações de sua empresa
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
Não é necessário ser preenchido, porém precisa  
estar presente na requisição.
{% endapi-method-parameter %}

{% api-method-parameter name="t" type="string" required=true %}
Grupo de entidades sobre o qual a busca será feita, neste caso "company".
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Dados da empresa retornados com sucesso.
{% endapi-method-response-example-description %}

```text
{
    "name": "Gestão Online",
    "nameLaw": "Gestao Online e Solucoes em Software LTDA",
    "document": "123123123",
    "email": "contato@gestao.plus",
    "cellphone": "12312313123",
    "phone": "123123123",
    "state": "GO",
    "city": "Goiania",
    "address": "Avenida Deputado Jamel Cecilio",
    "number": 0,
    "neighborhood": "Jardim Goias",
    "addressDetail": "Sala 1007ta QD B27 lt Area Ed. Brookfield Towers",
    "zipCode": "74810100",
    "image": {
        "name": "canivete-icon.jpg",
        "description": null,
        "href": "https://dev.gestao.plus/file?q=e2dvb2RfbG9va317ImRhdGEiOnsidXVpZCI6ImY0MjExOTc0LTg0NDAtMTFlYi1iNWZlLTAyNDJhYzExMDAwMyJ9LCJobWFjIjoiZTBjZGNkYTMwOWYxNzIwOTYxZjY1ZGI4MTg3MDBmNWRiYTM1YmNiYjdkYTA4MzFiNmUwOTE4MzlhNjk2ODI4ZSIsIm5vbmNlIjoiNTEyNDE2MjIwNjQ5NDUifQ=="
    },
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/order/info"
        }
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

