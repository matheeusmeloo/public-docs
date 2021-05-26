---
description: >-
  Os contatos de um parceiro são utilizados para registrar suas contas
  bancárias.
---

# Criar Contato

{% api-method method="post" host="https://api.gestao.plus" path="/user-contact" %}
{% api-method-summary %}
Criar contato do parceiro
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode adicionar um contato ao usuário.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
Url origem da requisição.
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token utilizado no formato "Bearer \(token\)".
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="accountDefault" type="string" required=true %}
true
{% endapi-method-parameter %}

{% api-method-parameter name="routingNumberCheckDigit" type="string" required=true %}
null
{% endapi-method-parameter %}

{% api-method-parameter name="routingNumber" type="string" required=true %}
0001
{% endapi-method-parameter %}

{% api-method-parameter name="bankCode" type="string" required=true %}
Código do banco do contato.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email do contato
{% endapi-method-parameter %}

{% api-method-parameter name="phone" type="string" required=true %}
6298377382
{% endapi-method-parameter %}

{% api-method-parameter name="birthDate" type="string" required=true %}
Data de nascimento ou null.
{% endapi-method-parameter %}

{% api-method-parameter name="document" type="string" required=true %}
CPF ou CNPJ
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Nome
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao criar contato.
{% endapi-method-response-example-description %}

```
{
    "name": "GESTAO ONLINE E SOLUCOES EM SOFTWARE LTDA",
    "document": "123123123",
    "birthDate": null,
    "phone": "12312312312",
    "cellphone": "12312312312",
    "email": "email@gestao.plus",
    "bankCode": "077",
    "routingNumber": "0001",
    "routingNumberCheckDigit": null,
    "accountType": "cc",
    "accountNumber": "123123123",
    "accountNumberCheckDigit": null,
    "accountDefault": true,
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-contact"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Token de acesso inválido.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



