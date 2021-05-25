# Login

{% api-method method="post" host="https://suaempresa.gestao.plus" path="/oauth" %}
{% api-method-summary %}
Login
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode logar no sistema enviando seus dados no corpo da requisição.  
Caso o login seja bem sucedido, você receberá um TOKEN de acesso para realizar futuras requisições.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=false %}
Origem da requisição
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
O seu nome de usuário \(Geralmente o CPF\)
{% endapi-method-parameter %}

{% api-method-parameter name="client\_secret" type="string" required=true %}
"app"
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
Logado com sucesso
{% endapi-method-response-example-description %}

```text
{
   "access_token":"SEU ACCESS TOKEN",
   "expires_in":"43200",
   "token_type":"Bearer",
   "scope":"",
   "refresh_token":"SEU REFRESH TOKEN"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Nome de usuário ou senha inválidos.
{% endapi-method-response-example-description %}

```
{
   "type":"http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
   "title":"invalid_grant",
   "status":401,
   "detail":"Invalid username and password combination"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Dados da requisição inválidos.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

