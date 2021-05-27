# Listar Parâmetros

{% api-method method="get" host="https://api.gestao.plus" path="/parameter" %}
{% api-method-summary %}
Listar parâmetros
{% endapi-method-summary %}

{% api-method-description %}
Esta rota permite que você liste os parâmetros de uma determinado sistema da url de origem no header.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Origin" type="string" required=true %}
URL de origem da requisição
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Sucesso ao listar parâmetros
{% endapi-method-response-example-description %}

```
{
    "_links": {
        "self": {
            "href": "https://api.gestao.plus/parameter"
        }
    },
    "_embedded": {
        "parameter": [
            {
                "dataKey": "public.parameters.agendamento",
                "dataValue": "presencial videoconferencia"
            },
            {
                "dataKey": "public.parameters.legendaAgendamento",
                "dataValue": "Selecione o tipo de agendamento, <br><br>\n\nSe você tem CNH (Carteira Nacional de Habilitação) agende seu atendimento por <b>videoconferência.</b>  <br>\nSe você não tem, agende seu atendimento <b>presencial</b> em uma de nossas lojas. <br>"
            },
            {
                "dataKey": "public.parameters.agendarValidacaoPresencial",
                "dataValue": "https://lrcontrole.com.br/sistema-soluti/agenda/agendamento.php"
            },
            {
                "dataKey": "public.parameters.agendarValidacaoVideoconferencia",
                "dataValue": "https://agendamento.videoconferencia.soluti.com.br/public-scheduling"
            },
            {
                "dataKey": "public.parameters.ajudaAgendamento",
                "dataValue": "https://cdn.gestao.plus/lp/assets/img/gif+turorial+videoconferencia+voucher.gif"
            },
            {
                "dataKey": "public.parameters.dadosIndicador",
                "dataValue": "indicador"
            },
            {
                "dataKey": "public.parameters.checkout.allowGuest",
                "dataValue": "1"
            },
            {
                "dataKey": "public.parameters.termos",
                "dataValue": "Este é um texto de teste.\nLorem ipsum dolor sit amet, consectetur adipisicing elit. Minus, id facilis. Iste impedit tempora fugit blanditiis obcaecati corporis accusamus rem explicabo cumque sit eius sunt at ullam cupiditate, quibusdam magnam?"
            }
        ]
    },
    "total_items": 8
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



