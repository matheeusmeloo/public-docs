# Geração de Relatórios

O sistema Gestão Online conta com um módulo específico para a geração e controle de relatórios, com toda a flexibilidade e rapidez que sua empresa precisa.

Para configurar relatórios pesquise pela página **`Widgets and Reports builder`**.
![](../../.gitbook/assets/3_relatorios.png)

## Como utilizar relatórios ?

Os casos mais comuns para a geração de relatórios são na página de **Vendas** e **Financeiro**, para gerar um relatório selecione uma das opções do menu superior direito da tela com o ícone de documento.

![](../../.gitbook/assets/1_relatorios.png)

![](../../.gitbook/assets/2_relatorios.png)

Ao clicar no relatório desejado um filtro será aberto, selecione as opções de filtragem que deseja utilizar para gerar o relatório \(unidades, período, cliente, vendedor\). Após preencher o filtro clique na opção **`Gerar Relatório`**, um documento será gerado em uma nova aba no caso de um pdf, ou será baixado caso seja uma planilha.

Geralmente, quando um relatório está sendo gerado serão necessárias duas datas, uma de início e outra de fim para determinar um período de consulta.

## Como criar relatórios?

Selecione a opção `Adicionar Item`, um formulário será aberto solicitando as informações do widget ou report.

{% hint style="info" %}
Os relatórios são gerados através de consultas MySQL e templates em XML, HTML ou Json definidos durante a sua criação. Os templates serão utilizados pelo motor gráfico responsável pela criação do relatório.
{% endhint %}

Para saber mais sobre como os widgets e relatórios funcionam, verifique o nosso manual de configurações clicando [aqui](https://github.com/Gestao-Online/public-docs/tree/ce2dcb553970e393c21b0336fbee8d426c99af31/ERP/iniciando/modulos/configuracoes/report.md).

