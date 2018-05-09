#### Cadastros e configurações

## Parametrização
Acesse o parâmetro de funcionamento na guia “Status” e defina os status abaixo:
  - Faturamento Solicitado à Órgão;
  - Faturamento Pendente;
  - NFe Compartilhada ao Órgão.
Esses status são utilizados durante o processamento das operações.

+ Transações para venda
  1. Crie uma transação para “Remessa por Conta e Ordem de Terceiros”:
     1. CFOPs 5923 / 6923:
     2. Esta transação não deve destacar impostos, de acordo com o Art. 266, §4º, b
     3. Marcar Movimenta Estoque.
     4. Desmarcar Gera Receber
     5. Desnarcar Venda à Ordem.

  2. Crie uma segunda transação para “Remessa Simbólica – Venda à Ordem”:
     1. CFOPs 5118 / 6118: Utilizados quando se tratar de produção do estabelecimento;
        CFOPs 5119 / 6119: Quando se tratar de mercadoria adquirida ou recebida de terceiros.
     2. Os impostos são tributados normalmente, quando devido.
     3. Desmarcar Movimenta Estoque
     4. Marcar Gera Receber
     5. Marcar Venda à Ordem

+ Transações para assistência
  1. Crie uma transação para “Remessa por Conta e Ordem de Terceiros”:
     1. CFOPs 5949 / 6949: Remessa de mercadoria por conta e ordem de terceiros, em bonificação à ordem.
     2. Marcar Movimenta Estoque
     3. Desmarcar Gera Receber.
     4. Desnarcar Venda à Ordem.

  2. Crie uma transação para “Remessa Simbólica”:
     1. CFOPs 5118 / 6118: Venda de produção do estabelecimento entregue ao destinatário por conta e ordem do adquirente originário,
      em venda à ordem – assistência técnica.
     2. Desmarcar “Movimenta Estoque”,
     3. Marcar Gera Receber.
     4. Marcar Venda à Ordem.

+ Transações para assistência bonificada
  1. Crie uma transação para “Remessa por Conta e Ordem de Terceiros”:
     1. CFOPs 5949 / 6949: Remessa de mercadoria por conta e ordem de terceiros, em bonificação à ordem.
     2. Marcar “Movimenta Estoque”
     3. Desmarcar Gera Receber
     4. Desmarcar Venda à Ordem

  2. Crie uma transação para “Remessa Simbólica”:
     1. CFOPs 5949 / 6949: Remessa de mercadoria por conta e ordem de terceiros, em bonificação à ordem.
     2. Desmarcar “Movimenta Estoque”.
     3. Marcar Gera Receber.
     4. Marcar Venda à Ordem.

* Cadastro de Mensagem para Nota Fiscal venda remessa simbólica
Crie uma mensagem para nota fiscal com o seguinte texto:

   > “Emitida nos termos do artigo xxx, §xx do RICMS/xxxx(ano) – XX(estado da empresa).

   Onde está “x” deve ser preenchido de acordo com o estado da empresa. Está mensagem deve ser vinculada ao parâmetro de funcionamento -> mensagens.
   Deve relacionar ao “Documento Referenciado”.

* Cadastro de Mensagem para Nota Fiscal assistência bonificada
Crie uma mensagem para nota fiscal com o seguinte texto:

   > “Produto bonificado tributado integralmente (ou isento) nos termos do art. xxx, §xx, da lei(ou RICMS) xxxx – XX(estado do fornecedor)”.

   Onde está “x” deve ser preenchido de acordo com o estado da empresa. Está mensagem deve ser vinculada ao parâmetro de funcionamento -> mensagens extras.

* Cadastro de Tags Características
Crie as tags características abaixo:
  1. Compartilhar Item(lógico): Uso obrigatório. Deve vincular aos itens que serão compartilhados com a MadeiraMadeira.
  2. Sequência de montagem(numérico): Uso opcional. Determina a sequência de montagem de produtos (relatório de Montagem x Sobras - PCP) em casos onde um mesmo volume é usado em mais de um produto.
  3. Quantidade máximo a montar(numérico): Uso opcional. Determina a quantidade máxima a montar do produto (relatório de Montagem x Sobras - PCP). Trabalha em conjunto com a tag anterior.
  4. Quantidade reservada à empresa(numérico): Uso opcional. Determina a quantidade de itens que será reservada à empresa.

    Acesse o cadastro de itens e faça o vínculo com as tags características.


#### Usuário

Acesse o cadastro do usuário, guia “Processamentos” e adicione todos os processamentos referente a integração com a MadeiraMadeira.

![](img/cad_usuario_processamentos.png)

Obs.: Somente realize está etapa se optar pela integração manual.

#### Tabela de preço
Crie duas tabelas de preço, uma para pedido de venda e a outra para assistência. Para cadastrar a tabela de preço deve seguir alguns critérios:

* Não permite “Lançar Descontos”;
* A condição de pagamento é a combinada com a MadeiraMadeira.

![](img/cad_tab_precos.png)

#### Cadastro do cliente Madeira Madeira
Para cadastrar o cliente MadeiraMadeira deve seguir alguns critérios para preenchimento das informações do padrão de compra:

* Tipo de frete: 2 – Terceiros;
* Opção do frete: Acessório;
* Condição Pagto: A prazo;
* Consultor de venda: Deve definir um consultor de venda padrão;
* Supervisor de venda: Caso não seja definido no cadastro do cliente, irá buscar o supervisor do cadastro do consultor de venda;
* Tabela de preço e condição de pagto: Deve definir a tabela de preço para pedido e assistência.

![](img/cad_cliente_mm.png)