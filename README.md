# Sistema Loja de Videogame

Desenvolvido por Tarcísio Luiz Harres de Almeida, na disciplina de Análise e Projeto de Sistemas (APS), do curso de Bacharelado em Ciência da Computação. 2026/2.

# 1. Descrição e delimitação do escopo

## 1.1 Descrição do sistema

O projeto consiste no desenvolvimento de um sistema de gerenciamento para uma loja de videogames, com o objetivo de organizar o catálogo de jogos, controlar o estoque e facilitar as operações de venda e aluguel.

A aplicação permitirá que administradores e funcionários cadastrem, consultem, atualizem e excluam informações sobre jogos e clientes, centralizando os dados em um único ambiente.

O sistema diferenciará os jogos destinados à venda, que possuem preço fixo e garantia, daqueles destinados ao aluguel, que possuem cobrança por diária e controle de disponibilidade.

## 1.2 Contexto de uso e público-alvo

O sistema será utilizado em uma loja especializada na venda e locação de jogos eletrônicos, tendo como público-alvo:

- **Administradores:** responsáveis pelo gerenciamento geral da loja e do catálogo.
- **Funcionários:** responsáveis pelo atendimento, registro de vendas e gerenciamento dos aluguéis.
- **Clientes:** usuários que utilizam os serviços de compra e locação.

A aplicação busca tornar as atividades diárias mais organizadas e eficientes.

## 1.3 Problema que o sistema busca resolver

O gerenciamento manual de uma loja de videogames pode ocasionar dificuldades no controle de estoque, na organização dos produtos e no acompanhamento das operações comerciais.

Entre os principais problemas estão a falta de centralização das informações, dificuldades para identificar jogos disponíveis e possíveis inconsistências nos registros de preços, garantias e aluguéis.

O sistema busca solucionar essas dificuldades por meio da informatização e organização dos processos.

## 1.4 Funcionalidades contempladas

O sistema contará com as seguintes funcionalidades:

- **Gerenciamento do catálogo:** cadastro, consulta, alteração e exclusão de jogos.
- **Controle de vendas:** gerenciamento de preços, garantias e estoque dos jogos comercializados.
- **Controle de aluguéis:** gerenciamento de valores por diária e disponibilidade dos jogos.
- **Gerenciamento de clientes:** cadastro, consulta, atualização e exclusão de clientes.
- **Controle de estoque:** acompanhamento da quantidade e disponibilidade dos produtos.
- **Consulta de informações:** pesquisa de jogos por suas características e modalidade de comercialização.

## 1.5 Delimitação do escopo

O projeto será limitado ao gerenciamento do catálogo de jogos, controle básico de estoque, cadastro de clientes e operações relacionadas à venda e ao aluguel.

Não serão contemplados inicialmente:

- Integração com bancos ou sistemas de pagamento.
- Emissão de notas fiscais eletrônicas.
- Controle contábil e financeiro completo.
- Integração com plataformas externas de jogos.
- Desenvolvimento de uma loja virtual.
- Sistemas de recomendação.
- Gerenciamento de fornecedores e compras.

Dessa forma, o sistema prioriza as funcionalidades essenciais para a organização e o gerenciamento de uma loja de videogames, mantendo a possibilidade de expansão futura.

# 2. Diagrama de Classes

> diagrama de classes conceitual

![Diagrama conceitual](./docs/Diagrama%20de%20Classes/Diagrama_de_classes_loja_videogames_conceitual.jpg)

> diagrama de classes domínio

![Diagrama de domínio](./docs/Diagrama%20de%20Classes/Diagrama_de_classes_loja_videogames_dominio.jpg)

# 3. [Documentação do Projeto](./Documentação%20do%20Projeto.md)
