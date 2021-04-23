# Sistema pré pago

Com este modulo é possível ter um maior controle financeiro sobre as suas unidades, sendo possível definir um saldo à conta de cada uma, debitar e definir um limite de vendas.

### Como funciona?

Para começar a usar o pré/pós pago é preciso cadastrar um contrato de controle sobre a mesma, assim será possível definir um valor limite a ela. Após o contrato ser concluido a unidade começara com o seu saldo vazio e cada movimentação feita pelos vendedores sobre ela aumentará ou decrementará seu valor baseado no tipo de movimentação em questão ex:(Aquisição de crédito ou Venda em pré pago). Para que as vendas nesse modelo funcionem as unidades devem possuir uma tabela específica para o pré-pago, caso o item a ser adicionado na venda não esteja presente nessa tabela o sistema levantará um erro.

### Cadastrando uma unidade ao pré pago

Para cadastrar uma unidade ao sistema pré-pago basta acessar a página `Contrato do controle Pré-Pago` e preencher os seguintes dados:

- Unidade *
- Empresa *
- Valor Limite *
- Data Validade *
- Status *

### Movimentações em pré pago

A unidade começara com o saldo zerado e limite estipulado previamente. Após cada venda o saldo é somado ao valor da movimentação e é apresentado um total com saldo + limite.

- Para adicionar um valor ao saldo da unidade é preciso realizar uma venda com um tipo de movimentação que atualize o pré pago como receita.

- Para remover uma quantia do saldo basta realizar uma venda com um tipo de movimentação que atualize o pré pago como despesa.

Dependendo do tipo de movimentação configurado pelo usuário a venda poderá ser registrada na página de controle somente após a baixa no financeiro.

##### Exemplo de venda para aquisição de crédito

<p align='center'>
  <img src='/ui/assets/venda-pre-pago.gif'/>
</p>

#### Resultado da venda no controle do pré pago

<p align='center'>
  <img src='/ui/assets/mudanca-pre-pago.png'/>
</p>

### Controle de acessos ao painel controle pré pago

Somente usuários com o perfil manager ou superior podem visualizar o saldo das unidades na página `controle pré-pago`