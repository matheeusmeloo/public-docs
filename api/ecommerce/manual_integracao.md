---
description: >-
  Esta integração pode ser feita copiando os links de cada produto presente no
  ecommerce gerado pelo sistema Gestão Online.
---

# Integração Manual

{% api-method method="get" host="https://seuecommerce.gestao.plus" path="/loja/checkout?p={}&lock=1&item={}&payload={}&callBackUrl={}" %}
{% api-method-summary %}
URL do Checkout
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode acessar o checkout de pagamentos.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="payload" type="string" required=true %}
Dados do usuário para o preenchimento automático do formulário, codificado para formato JSON e depois codificado para formato BASE64.
{% endapi-method-parameter %}

{% api-method-parameter name="item" type="string" required=true %}
SKU do produto dessa venda, codificado para formato JSON e depois codificado para formato BASE64.
{% endapi-method-parameter %}

{% api-method-parameter name="callBackUrl" type="string" required=true %}
URL de volta para o usuário retornar, se for necessário \(Opcional\)
{% endapi-method-parameter %}

{% api-method-parameter name="lock" type="string" required=true %}
Se definido, o cliente não poderá alterar quantidade de produtos, adicionar cupom de desconto.
{% endapi-method-parameter %}

{% api-method-parameter name="p" type="string" required=true %}
ID gerado dentro do sistema \(Opcional, consulte o administrador\)
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
URL de pagamento válida.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



