
#### Informações Importantes

* Obrigatório controlar estoque dos itens (Pedido e Assistência);
*  Atribuir no parâmetro de funcionamento do sistema os status “Faturamento Solicitado à órgão”, NFe “Compartilhada ao Órgão” e “Faturamento Pendente”;
*  Criar as transações para nota fiscal de remessa simbólica. Nesta transação deve desmarcar “Movimenta Estoque”, “marcar Gera Receber” e “Venda à Ordem”;
*  Criar as transações para nota fiscal por conta e ordem (acobertar o transporte). Nesta transação deve marcar “Movimenta Estoque” e desmarcar “Gera Receber” e “Venda à Ordem”;
+ Criar as tags características que serão vinculadas aos itens, são:
  1. Compartilhar Item(lógico): Obrigatório;
  2. Sequência de montagem(numérico): Opcional;
  3. Quantidade máximo a montar(numérico): Opcional;
  4. Quantidade reservada à empresa(numérico): Opcional. Obs.: Não definindo as tags opcionais, a sequência de montagem será aleatória, sempre irá montar o máximo
     e não terá estoque reservado a empresa.
* Vincular ao “Adquirente Original” a(s) tabela de preço(s) para pedido de venda e assistência, devendo especificar corretamente para o que estará disponível
  (Pedido de Venda e/ou Assistência);
* Configurar no “Padrões de Compra” do Adquirente Original a “Modalidade de Frete” como Terceiros e “Tipo Frete” como Acessórios;
* Faturamento via processamento específico: Na hipótese de erro de transmissão, não deve reprocessar documentos trocando a forma de emissão, deve-se aguardar reestabelecer o serviço (SEF) ou cancelar/inutilizar;
* Automatizando todo o processo via agendamento, é necessário instalar o certificado digital no servidor. Este certificado digital deve ser do tipo A1.