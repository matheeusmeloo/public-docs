# Atualizar Metadados do Usuário

{% api-method method="patch" host="https://api.gestao.plus" path="/user-metadata/:id" %}
{% api-method-summary %}
Atualizar metadados do usuário
{% endapi-method-summary %}

{% api-method-description %}
Rota utilizada para atualizar metadados do usuário. Alterar sua imagem de perfil.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID do usuário que terá suas informações alteradas.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
Origem da requisição
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authorization" type="string" required=true %}
Token de acesso para atualizar informações do usuário
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="dataValue" type="string" required=false %}
"novo conteudo em base64 aqui"
{% endapi-method-parameter %}

{% api-method-parameter name="dataKey" type="string" required=true %}
"picture"
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Alteração realizada com sucesso.
{% endapi-method-response-example-description %}

```
{
    "dataValue": "My new value",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user/108"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Erro ao validar access token.
{% endapi-method-response-example-description %}

```
{}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



