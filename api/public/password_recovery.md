# Recuperar Senha

{% api-method method="post" host="https://api.gestao.plus" path="/user?q=recovery-password" %}
{% api-method-summary %}
Recuperar Senha
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que o usuário altere a sua senha com o token e prefixo retornados anteriormente durante a solicitação.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
"recovery-password"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="password" type="string" required=true %}
Nova senha
{% endapi-method-parameter %}

{% api-method-parameter name="pinPrefix" type="string" required=true %}
Prefixo recebido juntamente com o PIN
{% endapi-method-parameter %}

{% api-method-parameter name="pin" type="string" required=true %}
PIN recebido por email ou sms
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=true %}
O seu token para recuperação da senha.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=202 %}
{% api-method-response-example-description %}
Senha alterada com sucesso.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unknown",
    "status": 202,
    "detail": {
        "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
        "title": "Password Recovery",
        "status": 202,
        "detail": "Password changed"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Senha ou token inválidos.
{% endapi-method-response-example-description %}

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "Invalid recovery password pin/token"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

