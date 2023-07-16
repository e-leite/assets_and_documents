Uma empresa enfrenta um problema na fase inicial de seu processo de vendas, envolvendo os setores de vendas composto por vendedores e gerentes e o departamento de atendimento composto por assistentes.
O processo de vendas segue o seguinte fluxo:
Após o fechamento das vendas o vendedor envia ao departamento de atendimento um formulário contendo os dados das vendas, por sua vez o assistente registra a venda no sistema ERP da empresa.
Atualmente, para enviar os pedidos ao departamento de atendimento os vendedores precisam preencher um formulário com os dados do pedido e para esse preenchimento eles precisam abrir outras planilhas para ver informações do cliente, lista de preços entre outras informações necessárias, isso torna o processo lento e trás incidência de registros com erros de digitação, dados fora de padrão, dados incompletos. Quando o formulário chega no departamento de atendimento causa dificuldade para compreensão dos dados ocasionando atraso no registro do pedido e consequentemente atraso nos processos seguintes.

A solução buscada pela empresa é o desenvolvimento de uma plataforma onde através do notebook ou smartphone o vendedor possa criar seu pedido de vendas apenas selecionando o cliente, produto, preço e posteriormente enviar para o departamento de atendimento  através de função disponível no software.

Espera-se uma solução que forneça:

## Criação de pedidos:

Deve ser realizada em uma tela intuitiva onde o usuário deve ter opção para seleção do cliente, local de faturamento, prazo de pagamento, data de entrega, tipo de frete. Para facilitar a seleção do cliente é necessário possibilitar busca por código ou nome. O local de faturamento deve ser um dropdown com opções, cada local de faturamento tem um prazo em dias para disponibilização da mercadoria, essa quantidade de dias deve ser somada à data do pedido para gerar a data de entrega e devem ser considerados dias úteis. Sobre o prazo de pagamento o cliente já possui essa informação em seu cadastro, porém ele pode optar por outro prazo para aquela compra, sendo assim o campo deve ser um dropdown com opções e quando o cliente for selecionado seu prazo de pagamento deve ser povoado como opção selecionada no dropdown, com isso o usuário poderá manter essa opção ou alterar caso necessário. O tipo de frete deve ser um radio button com opções “Por conta do cliente” ou “Por conta da empresa”, se for selecionado “Por conta do cliente” devem ser disponibilizados campo para informar o Nome da transportadora, Nome do contato da transportadora, Telefone da transportadora e E-mail da transportadora, se for selecionado a opção “Por conta da empresa” deve ser disponibilizado um campo opcional para inserir Link de localização, um radio button com a pergunta “Tem estrada de chão” e opções “Sim” e “Não”, se a opção for sim deve ser apresentado um campo numérico obrigatório para informar a quantidade de km de estrada de chão e deve haver um campo opcional para observação sobre o frete.

## Lista de pedidos:

Deve ser uma tela com tabela que mostre a lista de pedidos, deve haver um filtro por status do pedido para que o vendedor visualize separadamente os pedidos já enviados para o atendimento. Cada vendedor deve visualizar apenas seus pedidos. Essa tela deve dar acesso às funções de adicionar produtos, listar produtos, remover pedido, solicitar autorização e enviar pedido.

Inclusão de produtos ao pedido:

Deve ser realizada em uma tela contendo a lista de produtos para seleção, um dropdown com a categoria de produtos para filtro, um campo para busca de produtos por nome, um dropdown com as opções de faixa de preço e um campo numérico para inserir a quantidade do produto, também deve existir nesta tela um campo mostrando o preço unitário do produto selecionado e o preço total. Por regra da empresa a primeira faixa de preço é exclusiva para negociações diferenciadas, então somente pode ser usada mediante autorização, quando for selecionada a primeira faixa de preço não devem ser mostrados os preços unitários nem total, isso deve fazer com que o pedido somente possa ser liberado para envio após autorizado pelo Gerente.

## Listar produtos do pedido:

Deve ser uma tela que apresente os itens que estão inclusos no pedido com código, nome, quantidade, preço unitário e preço total. Deve haver opção para remover itens.

Enviar pedidos:

Deve ser uma tela tem a finalidade de conferência dos dados pelo vendedor antes de fazer o envio do pedido, deve conter id do pedido, nome do vendedor, código do cliente, nome do cliente, cidade do cliente, estado do cliente, base de faturamento, tipo de frete, data de entrega e prazo de pagamento, também deve constar a lista de produtos inclusos no pedido com seu código, nome, quantidade, preço unitário, preço total. Deve conter na tela um dropdown com as opções de e-mails dos responsáveis por recebimento de pedidos no departamento de atendimento.

## Dados manipulados pelo sistema:

### Lista de clientes:

O sistema não fará gestão de dados de clientes pois essa é uma função do ERP utilizado pela empresa, a lista de clientes será obtida deste ERP para que possa as informações possam ser utilizadas. O sistema fará a obtenção dos dados de clientes no banco de dados do sistema ERP, código do cliente, nome do cliente, cidade, estado e plano de pagamento.

### Lista de produtos e preços:

O sistema deve conter a lista com os produtos comercializados com código, nome, categoria, status (ativo ou inativo), preço de partida. Cada vendedor possui um mix de produtos para vendas e somente devem ter acesso aos produtos de seu mix. Toda administração dessa lista tais como atualização, inclusão de produtos, mudança de autorização de mix deve ser realizada pelo departamento de atendimento.


O projeto apresentado é a versão em NodeJs e Angular de uma aplicação que originalmente foi desenvolvida por mim utilizando Microsoft PowerApps, implementada e utilizada com sucesso neste ambiente.

