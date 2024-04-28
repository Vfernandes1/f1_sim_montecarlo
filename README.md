# Simulação de Corrida de Fórmula 1

Esta é uma simulação detalhada de corridas de Fórmula 1, utilizando objetos Python para modelar carros e corridas. O objetivo desta simulação é analisar o desempenho de carros fictícios em um campeonato de Fórmula 1, calculando probabilidades de vitória e a distribuição de pontuação com base nos resultados das corridas.

## Estruturas de Dados e Classes

### Classe `F1Car`
- **Atributos:**
  - `name`: Nome do carro, geralmente combinado com o nome da equipe e o modelo.
  - `max_speed`: Velocidade máxima que o carro pode atingir.
  - `acceleration`: Aceleração do carro.
  - `reliability`: Probabilidade de o carro não sofrer uma falha durante uma volta.

- **Método `simulate_lap_time`:**
  - Simula o tempo de volta do carro baseado nas condições da pista e na escolha dos pneus.
  - Fatores como falhas aleatórias e variações no desempenho do pneu são considerados para cada volta.

### Classe `Race`
- **Atributos:**
  - `cars`: Lista de carros (`F1Car`) participando da corrida.
  - `num_laps`: Número de voltas na corrida.
  - `track_conditions`: Condições da pista que podem variar (Dry, Wet, Icy).
  - `tires`: Dicionário definindo a eficácia dos pneus sob diferentes condições de pista.

- **Método `run_race`:**
  - Executa uma única corrida, calculando os tempos de volta para cada carro em cada volta e ordenando os carros pela performance. Pontuações são atribuídas com base na ordem de chegada.

## Funções Adicionais

### Função `championship`
- Executa um campeonato completo consistindo em várias corridas.
- Retorna os resultados do campeonato, contagem de vitórias por carro, e pontuações totais de cada carro.

### Função `analyze_results`
- Analisa os resultados do campeonato para calcular as probabilidades de vitória de cada carro.
- Retorna as probabilidades de vitória ordenadas.

## Função `main`
Esta função executa o campeonato utilizando uma lista predefinida de carros, coleta os resultados, e exibe as probabilidades de vitória e a distribuição da pontuação final através de gráficos. A função é projetada para ser autocontida e executável diretamente.

## Peculiaridades do Código

- **Modelagem de Falhas:** A confiabilidade influencia diretamente a chance de um carro completar uma volta sem falhas, adicionando um elemento de incerteza e realismo à simulação.
- **Influência dos Pneus:** Diferentes tipos de pneus têm eficácias variadas dependendo das condições da pista, o que afeta estratégias de corrida.
- **Visualização de Dados:** O uso de gráficos para visualizar os resultados finais e as probabilidades de vitória ajuda na interpretação dos dados gerados pela simulação.
- **Pontuação Dinâmica:** A pontuação é atribuída com base na posição de chegada em cada volta, acumulando ao longo da corrida, o que reflete um modelo mais próximo das corridas de resistência onde a consistência é recompensada.

## Referências

OpenAI. (2023). ChatGPT: Optimizing language models for dialogue. Recuperado de https://openai.com

Harris, C. R., Millman, K. J., van der Walt, S. J., et al. (2020). NumPy random module. In: NumPy v1.20 manual. Recuperado de https://numpy.org/doc/stable/reference/random/index.html

Croker, M. (2018). Using my Monte Carlo simulator to analyse 4x100m World Championships results. Medium. Recuperado de https://medium.com/@matthewcroker/using-my-monte-carlo-simulator-to-analyse-4x100mworld-championships-results-654639a308ac
