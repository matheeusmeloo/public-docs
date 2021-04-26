## Vendas

Cadastrar uma nova venda pelo Gestão Online é fácil, através dela é possível gerar boletos e emitir notas fiscais. Assim que uma venda é confirmada o estoque e financeiro são atualizados automaticamente.

Antes de cadastrar uma venda, a <a>empresa</a>, <a>cliente</a>, <a>produtos</a> e <a>tabela de preço</a> correspondente devem estar previamente cadastrados.

Pesquise pela página **`Vendas`**, após abrir, clique em "adicionar item" para realizar uma nova venda.

![Tela de vendas](/ui/assets/manuais-de-uso/vendas/1-venda.png)

### Realizando Venda

 Para que a venda seja realizada, primeiramente deve-se preencher somente os seguintes campos:

  - * Tipo de Negociação:
    Aqui escolhemos a forma de pagamento (boleto, cartão, dinheiro).
  - * Cliente cadastrado
  - * Tipo de Movimentação: Determina o comportamento da venda, se atualiza estoque, altera financeiro, faz parte do pré pago.

 
Após completar os campos, no menu principal da página clique em *`Salvar Rascunho`*

![Botão Salvar Rascunho](/ui/assets/manuais-de-uso/vendas/2-venda.png)

**Os outros campos serão preenchidos automaticamente após salvar rascunho.**

### Adicionando itens à venda

Após salvar o rascunho de sua venda, clique em *`adicionar item`* no menu de opções secundário dentro da aba itens.

![Adicionar item a venda](/ui/assets/manuais-de-uso/vendas/3-vendas.png)

Complete os campos relacionados ao item:

- Produto/serviço: Digite qual certificado deseja vender, ao selecioná-lo o sistema puxa automaticamente o valor de acordo com a 'tabela de preço' cadastrada no vendedor que esta realizando a venda,
- Quantidade: Escolha a quantidade de certificados, mesmo sendo mais de '1' certificado o valor exibido será referente a '1' unidade.
- Caso o 'Produto/serviço' seja um *KIT: Ao selecionar o KIT, será puxado pelo sistema o '*local de estoque' que está cadastrado no vendedor, onde então, de forma automática, vai ser descontado a quantidade de 'Token, SmartCard ou Leitora'  de acordo com a quantidade selecionada.
- Se deseja adicionar um desconto ao 'produto/serviço' do seu cliente, selecione o desconto em percentual ou em valor.  O valor ou percentual selecionado será descontado de cima de cada certificado.
- Em seguida clique em ''salvar'' para gravar a venda.

![Adicionar item a venda](/ui/assets/manuais-de-uso/vendas/4-vendas.png)

- logo depois clique em ''confirmar'' logo acima na cor  'verde'.

{% hint style='warning' %}
**Cuidado**: Os valores de uma venda assim como o seu desconto não podem ser alterados após a sua liberação/confirmação. Estes dados podem ser modificados enquanto a venda for um rascunho.
{% endhint %} 

### Gerar boleto

- Clique em 'gerar boleto' em seguida 'emitir boletos', o boleto gerado em seguida irá para aba 'anexos'.

<p align='center'>
  <img src='/ui/assets/capturas-de-tela/gerar-boleto.gif'/>
<p>

- O Link de pagamento é gerado nesse ícone. 

<p align='center'>
  <img src='/ui/assets/capturas-de-tela/botao-link.png'/>
<p>

Cópie o Link e encaminhe para o cliente. A forma de pagamento do cliente em Link de pagamento é definida no 'Tipo de Negociação' ao realizar a venda.

O financeiro será baixado automaticamente caso a venda tenha sido realizada utilizando o  'Tipo de negociação': Boleto ou Cartão.
Caso não possua o Go-pag, o seu Banco devera ter integração com o Gestão.Online para que essa baixa seja automática.
Sem a integração do banco no Gestão.online, pagamentos em dinheiro, maquininha física, PIX ou outra forma de pagamento sem vínculo com o sistema, a Baixa devera ser manual:

<p align='center'>
  <img src='/ui/assets/capturas-de-tela/baixa-manual-vendas.gif'/>
<p>

### Para cancelar a venda

Se caso o cliente desistiu de fazer a compra antes de ter a 'baixa' no financeiro.

- Clique em 'cancelar' em seguida escreva o motivo do cancelamento.

<p align='center'>
  <img src='/ui/assets/capturas-de-tela/cacelamento-vendas.gif'/>
<p>


### Se já estiver feito a baixa no financeiro.

- Entre na aba do 'financeiro', clique para editar venda logo clique em 'estornar'.

<p align='center'>
  <img src='/ui/assets/capturas-de-tela/estornar-financeiro.gif'/>
<p>