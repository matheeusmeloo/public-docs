# Login

{% api-method method="post" host="https://api.gestao.plus" path="/oauth" %}
{% api-method-summary %}
Login
{% endapi-method-summary %}

{% api-method-description %}
Através desta rota o seu parceiro é capaz de logar na api, um **token** será devolvido como resposta para que ele possa realizar futuras requisições em rotas privadas.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=false %}
https://suaempresa.gestao.plus
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=true %}
A sua senha
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=true %}
O seu nome de usuário geralmente o CPF
{% endapi-method-parameter %}

{% api-method-parameter name="client\_secret" type="string" required=true %}
null
{% endapi-method-parameter %}

{% api-method-parameter name="client\_id" type="string" required=true %}
"app"
{% endapi-method-parameter %}

{% api-method-parameter name="grant\_type" type="string" required=true %}
"password"
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Login realizado com sucesso.
{% endapi-method-response-example-description %}

```text
{
    "access_token": "SEU TOKEN",
    "expires_in": "43200",
    "token_type": "Bearer",
    "scope": "",
    "refresh_token": "SEU REFRESH TOKEN"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Corpo da requisição inválido.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "invalid_client",
    "status": 400,
    "detail": "DESCRIÇÃO SOBRE O ERRO"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Credenciais inválidas.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "invalid_grant",
    "status": 401,
    "detail": "Invalid username and password combination"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

