# Esqueci Minha Senha \(SMS\)

{% api-method method="post" host="https://suaempresa.gestao.plus" path="/user?q=forgot-password" %}
{% api-method-summary %}
Resetar Senha \(SMS\)
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
forgot-password
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="cellphone" type="string" required=true %}
O seu número de celular
{% endapi-method-parameter %}

{% api-method-parameter name="document" type="string" required=true %}
O seu CPF
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Atualmente só retorna erro mesmo enviando código pin para o usuário.
{% endapi-method-response-example-description %}

```
{
    "trace": [
        {
            "file": "/var/www/module/IUPBase/src/EventListener/AbstractListener.php",
            "line": 420,
            "function": "preCreate",
            "class": "IUPBase\\V1\\EventListenerController\\User",
            "type": "->",
            "args": [
                {
                    "document": "70434612197",
                    "cellphone": "62985499507"
                }
            ]
        }
    ],
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Internal Server Error",
    "status": 500,
    "detail": "Call to a member function getId() on null"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



