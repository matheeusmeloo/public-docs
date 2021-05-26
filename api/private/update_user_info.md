# Atualizar Informações do Usuário

{% api-method method="patch" host="https://api.gestao.plus" path="/user/:id" %}
{% api-method-summary %}
Atualizar informações do usuário
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que você atualize os dados de um determinado usuário, enviando os novos dados dentro do corpo da requisição.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
Origem da requisição.
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}

{% api-method-parameter name="Authentication" type="string" required=true %}
Token de autenticação gerado durante o login
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="vendedor" type="string" required=false %}
ID do Vendedor \(opcional\)
{% endapi-method-parameter %}

{% api-method-parameter name="token" type="string" required=false %}
Token do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="tipoPessoa" type="string" required=false %}
Tipo de Pessoa \(PF ou PJ\)
{% endapi-method-parameter %}

{% api-method-parameter name="telefoneComercial" type="string" required=false %}
Telefone Comercial
{% endapi-method-parameter %}

{% api-method-parameter name="telefone" type="string" required=false %}
Telefone
{% endapi-method-parameter %}

{% api-method-parameter name="tabelaDePrecoVendaOnline" type="string" required=false %}
Tabela de preço para o ecommerce do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="razaoSocial" type="string" required=false %}
Razão Social
{% endapi-method-parameter %}

{% api-method-parameter name="numero" type="string" required=false %}
Numero
{% endapi-method-parameter %}

{% api-method-parameter name="nome" type="string" required=false %}
Nome
{% endapi-method-parameter %}

{% api-method-parameter name="nfseRetemIss" type="string" required=false %}
Flag caso o parceiro seja substituto tributário
{% endapi-method-parameter %}

{% api-method-parameter name="linkVendaOnline" type="string" required=false %}
Link para o ecommerce do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="inscricaoMunicipal" type="string" required=false %}
Inscrição Municipal
{% endapi-method-parameter %}

{% api-method-parameter name="inscricaoEstadual" type="string" required=false %}
Inscrição Estadual
{% endapi-method-parameter %}

{% api-method-parameter name="imagem" type="string" required=false %}
Imagem do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=false %}
Identificador do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="geraLinkVendaOnline" type="string" required=false %}
Flag para geração de link para o parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="estado" type="string" required=false %}
Estado
{% endapi-method-parameter %}

{% api-method-parameter name="endereco" type="string" required=false %}
Endereço
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
Email
{% endapi-method-parameter %}

{% api-method-parameter name="descricaoDaParceiria" type="string" required=false %}
Descrição da parceria
{% endapi-method-parameter %}

{% api-method-parameter name="descricao" type="string" required=false %}
Descrição
{% endapi-method-parameter %}

{% api-method-parameter name="cpfCnpj" type="string" required=false %}
CPF ou CNPJ
{% endapi-method-parameter %}

{% api-method-parameter name="complemento" type="string" required=false %}
Complemento
{% endapi-method-parameter %}

{% api-method-parameter name="codigoIbge" type="string" required=false %}
Código IBGE
{% endapi-method-parameter %}

{% api-method-parameter name="cidade" type="string" required=false %}
Cidade
{% endapi-method-parameter %}

{% api-method-parameter name="cep" type="string" required=false %}
CEP
{% endapi-method-parameter %}

{% api-method-parameter name="celular" type="string" required=false %}
Celular
{% endapi-method-parameter %}

{% api-method-parameter name="categoriaParceiro" type="string" required=false %}
Categoria do parceiro
{% endapi-method-parameter %}

{% api-method-parameter name="bairro" type="string" required=false %}
Bairro
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao alterar informações de usuário.
{% endapi-method-response-example-description %}

```
{
    "address": "My new address",
    "zipCode": "74000000",
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/user/108"
        }
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Erro ao atualizar campo solicitado.
{% endapi-method-response-example-description %}

```
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "You cannot change the field: fieldname"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Access Token Inválido.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



