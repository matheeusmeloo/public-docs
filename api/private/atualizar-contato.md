# Atualizar Contato

{% api-method method="patch" host="https://api.gestao.plus" path="/user-contact/:id" %}
{% api-method-summary %}
Atualizar o contato
{% endapi-method-summary %}

{% api-method-description %}
Com esta rota você pode atualizar as informações de um contato.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID do contato que terá seus dados alterados
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
Access Token no formato \(Bearer {token}\)
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="Atributo do Contato" type="string" required=false %}
Preencha o valor do atributo correspondente ao contato aqui.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Dados do contato alterados com sucesso.
{% endapi-method-response-example-description %}

```
{
    "phone": "62123",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user-contact/20"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Sem permissão para alterar o contato.
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (indicator scope)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



