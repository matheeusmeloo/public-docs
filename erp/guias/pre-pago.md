# Sistema Pré/Pós pago

Com este modulo é possível ter um maior controle financeiro sobre as suas unidades, sendo possível definir um saldo à conta de cada uma, debitar e definir um limite de vendas.

## Como funciona?

Para começar a usar o pré/pós pago é preciso cadastrar um contrato de controle sobre a unidade, assim será possível definir um valor limite a ela. Após o contrato ser concluido a unidade começa com o seu saldo vazio e cada movimentação feita pelos vendedores altera o seu saldo baseado no **`tipo de movimentação`** em questão ex:\(**Aquisição de crédito** ou **Venda Pré\_Pago**\). Para que as vendas nesse modelo funcionem as unidades devem possuir uma tabela específica para o pré\_pago, caso o item a ser adicionado na venda não esteja presente nessa tabela o sistema acusa um erro.

## Como adicionar o modelo pré/pós pago à uma unidade?

Para isso basta acessar a página `Contrato do controle Pré_Pago` e preencher os seguintes dados:

* Unidade \*
* Empresa \*
* Valor Limite \*
* Data Validade \*
* Status \*

## Movimentações em pré pago

A unidade começa com o saldo zerado e limite estipulado previamente. Após cada venda o saldo é somado ao valor da movimentação e é apresentado um total com saldo + limite.

* Para adicionar um valor ao saldo da unidade é preciso realizar uma venda com um tipo de movimentação que atualize o pré pago como receita.
* Para remover uma quantia do saldo basta realizar uma venda com um tipo de movimentação que atualize o pré pago como despesa.

Dependendo do tipo de movimentação configurado pelo usuário a venda poderá ser registrada na página de controle somente após a baixa no financeiro.

#### Exemplo de venda para aquisição de crédito

![](https://github.com/Gestao-Online/public-docs/tree/ce2dcb553970e393c21b0336fbee8d426c99af31/ERP/assets/capturas_de_tela/venda_pre_pago.gif)

### Resultado da venda no controle do pré pago

![](https://github.com/Gestao-Online/public-docs/tree/ce2dcb553970e393c21b0336fbee8d426c99af31/ERP/assets/capturas_de_tela/mudanca_pre_pago.png)

## Controle de acessos ao painel controle pré pago

Somente usuários com o perfil manager ou superior podem visualizar o saldo das unidades na página `controle pré-pago`

