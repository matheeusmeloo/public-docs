# Esqueci Minha Senha \(Email\)

{% api-method method="post" host="https://api.gestao.plus" path="/user?q=forgot-password" %}
{% api-method-summary %}
Resetar Senha \(Email\)
{% endapi-method-summary %}

{% api-method-description %}
Com essa rota é possível desenvolver um fluxo de recuperação de senhas.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
"application/json"
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="q" type="string" required=true %}
Ação que deseja fazer sobre o usuário \(Query\). Neste caso "forgot-password"
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="document" type="string" required=true %}
O CPF do usuário
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
O email da conta que deseja recuperar a senha
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=202 %}
{% api-method-response-example-description %}
Sucesso ao solicitar troca de senha.
{% endapi-method-response-example-description %}

```text
{
    "pinPrefix": "PREFIXO DE PIN",
    "token": "TOKEN PARA RECUPERAÇÃO DE SENHA",
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forgot Password",
    "status": 202,
    "detail": "Email sent"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
Erro ao solicitar troca de senha \(Requisição incorreta ou email inválido\)
{% endapi-method-response-example-description %}

```text
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
                    "email": "CÓDIGO DE EMAIL"
                }
            ]
        },
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

