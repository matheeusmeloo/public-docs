# Recuperar Senha

{% api-method method="post" host="https://api.gestao.plus" path="/user?q=recovery-password" %}
{% api-method-summary %}
Recuperar Senha
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que o usuário recupere sua senha utilizando o código de resposta das rotas anteriores.
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
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```text
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

