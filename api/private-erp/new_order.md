# Criar Pedido

{% api-method method="post" host="https://api.gestao.plus" path="/order-external" %}
{% api-method-summary %}
Criar um novo pedido
{% endapi-method-summary %}

{% api-method-description %}
Nesta rota você pode adicionar um contato ao usuário.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-api-key" type="string" required=true %}
Token de acesso ERP
{% endapi-method-parameter %}

{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="code" type="string" required=false %}
Código de identificação da venda
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="string" required=false %}
Data da venda: Y-m-d H:i:s 
{% endapi-method-parameter %}

{% api-method-parameter name="utmCampaign" type="string" required=false %}
UTM Campaign
{% endapi-method-parameter %}

{% api-method-parameter name="utmId" type="string" required=false %}
UTM ID
{% endapi-method-parameter %}

{% api-method-parameter name="utmMedium" type="string" required=false %}
UTM Medium
{% endapi-method-parameter %}

{% api-method-parameter name="utmSource" type="string" required=false %}
UTM Source
{% endapi-method-parameter %}

{% api-method-parameter name="user" type="object" required=true %}
Objeto com os dados do cliente
{% endapi-method-parameter %}

{% api-method-parameter name="orderItems" type="array" required=true %}
Array de itens
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Criação do pedido com sucesso.
{% endapi-method-response-example-description %}

```json
{
    "code": "SUCCESS_ORDER_CREATED",
    "data": {
        "publicToken": "OMzMyMQ_MTY4OTYyMjM4MDUEaa1xNjE_7C44FWNkaVR-GJB871Mb2g",
        "orderCode": "CÓDIGO_DA_VENDA",
        "orderId": "ID_DA_VENDA"
    },
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Unknown",
    "status": 201,
    "detail": "ok"
}

```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Token do ERP inválido.
{% endapi-method-response-example-description %}

```json
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden, invalid key (x-api-key)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Exemplo de corpo da requisição:

#### Detalhando "user":

```json
{
    "user": { // Dados do cliente
        "name": "required", // Nome
        "nameLaw": "", // Razão Social
        "email": "required", // E-mail
        "document": "required", // Documento
        "cellphone": "", // Celular
        "phone": "", // Telefone
        "stateRegistration": "", // Inscrição estadual
        "zipCode": "", // CEP
        "address": "", // Endereço
        "number": "", // Número
        "neighborhood": "", // Bairro
        "addressDetail": "", // Complemento
        "city": "", // Cidade
        "state": "" // Estado
    }
```

#### Detalhando "orderItems":

```json
{
    "orderItems": [
        {
            "product": "required", // SKU do produto
            "quantity": "required", // Quantidade
            "price": "", // Valor desse item
            "discount": "" // Desconto nesse item (R$)
        }
    ]
```

### Exemplo completo do corpo da requisição
```json
{
    "code": "",
    "date": "",
    "note": "",
    "user": {
        "name": "",
        "nameLaw": "",
        "email": "",
        "document": "",
        "cellphone": "",
        "phone": "",
        "stateRegistration": "",
        "zipCode": "",
        "address": "",
        "number": "",
        "neighborhood": "",
        "addressDetail": "",
        "city": "",
        "state": ""
    },
    "orderItems": [
        {
            "product": "",
            "quantity": "",
            "price": "",
            "discount": ""
        }
    ]
}
```