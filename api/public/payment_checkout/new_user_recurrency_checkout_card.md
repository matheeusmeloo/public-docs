---
description: >-
  Com o checkout de recorrência fornecido pelo Gestão Online, o seu cliente só
  precisa realizar o pagamento uma única vez para que nos meses subsequentes a
  venda seja registrada automaticamente.
---

# Checkout Recorrência Novo Usuário \(Cartão de Crédito\)

{% api-method method="post" host="https://api.gestao.plus" path="/order?t={token}" %}
{% api-method-summary %}
Checkout de recorrência para novo usuário pagando no cartão
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que você acesse o checkout como um novo usuário pagando no cartão de crédito.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="t" type="string" required=true %}
Token para acesso a rota.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="items" type="string" required=true %}
Lista de produtos adicionados ao checkout, com o seu id e quantidade.
{% endapi-method-parameter %}

{% api-method-parameter name="userData" type="string" required=true %}
Dados do usuário
{% endapi-method-parameter %}

{% api-method-parameter name="type" type="string" required=true %}
Tipo do pedido, recorrência.
{% endapi-method-parameter %}

{% api-method-parameter name="negotiationType" type="string" required=true %}
ID do tipo de negociação escolhido.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao solicitar checkout.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token de acesso inválido.
{% endapi-method-response-example-description %}

```
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

#### Exemplo de corpo da requisição

```text
{
    "negotiationType": "8",
    "type": "R",
    "userData": {
        "document": "123123123",
        "name": "GERADO",
        "email": "gestao@live.com",
        "cellphone": "(62) 123123-8359",
        "zipCode": "74230-130",
        "address": "Avenida T 14",
        "number": "1111",
        "neighborhood": "Setor Teste",
        "addressDetail": "Apt 123123",
        "city": "Goiânia",
        "state": "GO"
    },
    "items": [
        {
            "id": "83",
            "quantity": 1
        }
    ]
}
```

