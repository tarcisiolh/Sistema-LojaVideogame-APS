# Documento de Especificação de Requisitos

## 1. Requisitos Funcionais

O que o sistema deve fazer — as funcionalidades que ele deve oferecer.

| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| RF01 | O sistema deve permitir cadastrar um jogo informando, no mínimo: nome, gênero, plataforma, classificação indicativa, data de lançamento e desenvolvedora. | Alta | — |
| RF02 | O sistema deve permitir consultar os jogos cadastrados. | Alta | RF01 |
| RF03 | O sistema deve permitir alterar os dados de um jogo já cadastrado. | Alta | RF01 |
| RF04 | O sistema deve permitir excluir um jogo, desde que ele não possua venda ou locação em andamento vinculada. | Média | RF01, RF11, RF12 |
| RF05 | O sistema deve permitir classificar cada registro de jogo como destinado à venda ou ao aluguel. | Alta | RF01 |
| RF06 | Para jogos destinados à venda, o sistema deve permitir registrar preço de venda, prazo/condição de garantia e quantidade em estoque. | Alta | RF05 |
| RF07 | Para jogos destinados ao aluguel, o sistema deve permitir registrar o valor da diária e a quantidade de cópias disponíveis para locação. | Alta | RF05 |
| RF08 | O sistema deve permitir cadastrar clientes informando, no mínimo, nome e um meio de contato. | Alta | — |
| RF09 | O sistema deve permitir consultar, alterar e excluir cadastros de clientes, impedindo a exclusão quando houver operação em andamento vinculada. | Média | RF08, RF11, RF12 |
| RF10 | O sistema deve permitir registrar uma venda, associando o cliente, o jogo, a quantidade, a data e o meio de pagamento. | Alta | RF06, RF08 |
| RF11 | Ao confirmar uma venda, o sistema deve reduzir do estoque a quantidade vendida e impedir a operação quando não houver quantidade suficiente. | Alta | RF10 |
| RF12 | O sistema deve permitir registrar uma locação, associando cliente, jogo, data de retirada, data prevista de devolução e valor da diária. | Alta | RF07, RF08 |
| RF13 | O sistema deve impedir o registro de locação quando não houver cópia disponível do jogo no período solicitado. | Alta | RF12 |
| RF14 | O sistema deve permitir registrar a devolução de um jogo alugado, atualizando sua situação para disponível quando não houver outra restrição de disponibilidade. | Alta | RF12 |
| RF15 | O sistema deve permitir consultar as locações em andamento e suas respectivas datas previstas de devolução. | Média | RF12 |
| RF16 | O sistema deve apresentar a disponibilidade e a quantidade em estoque dos jogos conforme a modalidade selecionada (venda ou aluguel). | Alta | RF06, RF07, RF11, RF12, RF14 |

## 2. Requisitos Não Funcionais

Políticas, normas e condições estabelecidas pela empresa que devem ser respeitadas na execução das funcionalidades.

| ID | Descrição | Categoria | Prioridade | Depende de |
|---|---|---|---|---|
| RNF01 | As consultas e operações comuns do sistema devem apresentar resposta em até 3 segundos, em condições normais de uso. | Desempenho | Alta | — |
| RNF02 | O sistema deve permitir pelo menos 20 usuários internos simultâneos sem interrupção das operações principais. | Desempenho | Média | — |
| RNF03 | O acesso às funções de cadastro, alteração, exclusão e registro de operações deve exigir autenticação do usuário. | Segurança | Alta | — |
| RNF04 | As senhas dos usuários devem ser armazenadas utilizando mecanismo de hash apropriado, nunca em texto puro. | Segurança | Alta | RNF03 |
| RNF05 | O sistema deve validar os campos obrigatórios e apresentar mensagens que identifiquem claramente os dados inválidos ou ausentes. | Usabilidade | Alta | — |
| RNF06 | A interface deve manter organização visual consistente e permitir a utilização das funções principais por funcionários sem conhecimento técnico especializado. | Usabilidade | Média | — |
| RNF07 | O código deve ser organizado em módulos, separando, no mínimo, as responsabilidades de interface, regras de negócio e acesso aos dados. | Manutenibilidade | Média | — |
| RNF08 | Os dados cadastrados devem ser armazenados de forma persistente, permanecendo disponíveis após o encerramento e a reinicialização da aplicação. | Confiabilidade | Alta | — |
| RNF09 | O sistema deve realizar cópias de segurança dos dados ao menos uma vez ao dia, permitindo sua recuperação em caso de falha. | Confiabilidade | Média | RNF08 |

## 3. Regras de Negócio

Definem políticas e restrições próprias do funcionamento da loja, que devem ser respeitadas pelo sistema.

| ID | Descrição | Prioridade | Depende de |
|---|---|---|---|
| RN01 | Um jogo só pode ser vendido se estiver classificado para venda e houver quantidade suficiente em estoque. | Alta | RF05, RF06, RF10, RF11 |
| RN02 | Um jogo só pode ser alugado se estiver classificado para aluguel e houver ao menos uma cópia disponível durante todo o período solicitado. | Alta | RF07, RF12, RF13 |
| RN03 | O valor de uma locação deve ser calculado com base no valor da diária cadastrada para o jogo e na quantidade de diárias do período contratado. | Alta | RF07, RF12 |
| RN04 | Uma cópia de jogo alugada somente volta a ser considerada disponível após o registro de sua devolução. | Alta | RF12, RF14 |
| RN05 | Preço de venda e valor da diária não podem ser valores negativos; a quantidade em estoque deve ser um número inteiro igual ou superior a zero. | Alta | RF06, RF07 |
| RN06 | Um jogo ou cliente que possua operação em andamento vinculada não pode ser excluído do cadastro. | Média | RF04, RF09, RF12 |
