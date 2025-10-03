# Descrição do Projeto

Este projeto visa analisar a **retenção de usuários** em uma plataforma de compras online ao longo do tempo, utilizando uma análise de **coorte**. O objetivo é calcular a taxa de retenção de usuários em função de suas coortes de compra, ou seja, grupos de usuários que realizaram sua primeira compra em um mesmo mês.

A análise é realizada utilizando uma base de dados de pedidos de usuários, onde as compras são agrupadas por coortes (baseado no mês da primeira compra) e a retenção de usuários é medida ao longo dos meses seguintes. A taxa de retenção é então visualizada em um gráfico de calor para facilitar a análise dos padrões ao longo do tempo.

## Ferramentas e Bibliotecas Utilizadas

- **pandas**: Manipulação e análise de dados.
- **numpy**: Cálculos numéricos.
- **seaborn**: Visualização de dados (geração do gráfico de calor).
- **matplotlib**: Geração de gráficos e visualizações.
- **operator**: Utilização da função `attrgetter` para cálculo da diferença de períodos.

## Metodologia

1. **Pré-processamento**:
   - Padronização dos nomes das colunas para o formato `snake_case`.
   - Conversão das datas de compra para o formato datetime.
   - Criação de colunas adicionais para identificar o **mês da primeira compra** e o **índice de coorte**, que indica o número de meses desde a primeira compra de um usuário.

2. **Análise dos Dados**:
   - Agrupamento dos dados por **mês da primeira compra** (coorte) e **índice de coorte** (meses após a primeira compra).
   - Cálculo do número de usuários únicos para cada coorte e mês.
   - Cálculo da taxa de retenção como a razão entre o número de usuários ativos em cada mês e o número de usuários na primeira compra de cada coorte.

3. **Visualização**:
   - A taxa de retenção é visualizada por meio de um **gráfico de calor**, onde cada célula mostra a porcentagem de retenção de uma coorte em um determinado mês.

## Resultados

A análise resulta em uma **visualização de retenção de usuários** ao longo do tempo, permitindo identificar padrões e tendências nas compras repetidas de usuários. O gráfico de calor gerado ajuda a visualizar como a retenção diminui à medida que o tempo passa desde a primeira compra, fornecendo insights sobre a fidelidade do cliente.

## Aprendizados

- **Taxa de retenção**: A análise de coorte permite medir a fidelidade dos usuários ao longo do tempo, identificando possíveis áreas de melhoria para estratégias de retenção.
- **Padrões de comportamento**: A visualização ajuda a identificar os meses em que a retenção de usuários é mais forte ou mais fraca, permitindo que a plataforma ajuste suas estratégias de marketing ou engajamento com base nesses dados.
