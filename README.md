# Gestão de Leitos Hospitalares usando Otimização com Pyomo

Este projeto visa otimizar a gestão de leitos hospitalares utilizando técnicas de otimização matemática com a biblioteca [Pyomo](http://www.pyomo.org/). O código está implementado em um **notebook** no Google Colab, onde são simuladas diferentes alocações de pacientes a leitos com base em critérios de gravidade, tempo de permanência e capacidade dos leitos.

## Objetivo

O objetivo deste projeto é demonstrar como técnicas de **Pesquisa Operacional** podem ser aplicadas à alocação eficiente de recursos hospitalares, como leitos de UTI e enfermaria. Utilizando um modelo de **programação inteira mista**, garantimos que pacientes sejam alocados de forma a minimizar o tempo de internação e respeitar as restrições de capacidade.

## Estrutura do Notebook

O notebook contém as seguintes seções:

1. **Instalação das Dependências**:
   - Instalação de **Pyomo** e **GLPK** para resolver o modelo de otimização.
   
2. **Geração de Instâncias**:
   - Geração de instâncias fictícias de pacientes e leitos hospitalares. Cada instância simula diferentes combinações de gravidade e tempos de permanência dos pacientes.
   
3. **Formulação do Modelo de Otimização**:
   - Definição das variáveis de decisão, função objetivo e restrições do problema de alocação de leitos.

4. **Execução de Múltiplas Instâncias**:
   - Execução do modelo para diferentes instâncias geradas aleatoriamente, com tratamento de casos inviáveis.

5. **Resultados**:
   - Impressão dos resultados, mostrando quais pacientes foram alocados a quais leitos e o valor da função objetivo (tempo de permanência ponderado pela gravidade).

## Como Executar no Google Colab

### Executando o Projeto

1. Abra o notebook no Google Colab clicando [aqui](https://colab.research.google.com/drive/1bGHuJtD3mfqaZMOdhfdUKOyuOlbgllHs?usp=sharing).
   
2. Execute as células na ordem sequencial para:
   - Instalar as dependências.
   - Gerar as instâncias.
   - Rodar o modelo de otimização.
   - Ver os resultados das diferentes execuções de instâncias.

3. As saídas de cada execução mostram:
   - A instância gerada (pacientes, leitos, gravidade, e capacidade).
   - Alocação de pacientes aos leitos.
   - Se uma instância for inviável, uma mensagem de erro será mostrada, e o código continua com a próxima instância.

## Requisitos

- **Google Colab** ou ambiente Jupyter Notebook local.
- **Python 3**
- **Pyomo**: Biblioteca para modelagem de otimização.
- **GLPK**: Solver utilizado para resolver o modelo de otimização.
