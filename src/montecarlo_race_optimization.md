# Simulação de Corridas de Fórmula 1 - Otimizado

Esta atividade permite simular um campeonato de Fórmula 1, levando em conta diversos fatores realistas que influenciam o desempenho dos carros e o resultado das corridas.

## Classes e Funções

### `F1Car`

**Descrição**: Representa um carro de Fórmula 1 com características específicas de desempenho e condições de corrida.

**Atributos**:
- `name`: Nome do carro.
- `max_speed`: Velocidade máxima que o carro pode alcançar.
- `acceleration`: Aceleração do carro.
- `reliability`: Confiabilidade do carro, afetando a probabilidade de falhas mecânicas.
- `fuel_capacity`: Capacidade de combustível do carro.
- `fuel_level`: Nível atual de combustível.
- `tire_wear`: Desgaste atual dos pneus.

**Métodos**:
- `__init__`: Inicializa um novo carro com as especificações fornecidas.
- `simulate_lap_time`: Calcula o tempo de uma volta com base nas condições atuais do carro e da pista.
- `pit_stop`: Realiza um pit stop para trocar pneus e reabastecer combustível.

### `Race`

**Descrição**: Gerencia a execução de uma corrida, incluindo várias voltas e condições dinâmicas como condições meteorológicas.

**Atributos**:
- `cars`: Lista de carros participantes na corrida.
- `num_laps`: Número de voltas na corrida.
- `track_conditions`: Condições possíveis da pista (Seco, Molhado, Gelado).
- `tires`: Tipos de pneus disponíveis para diferentes condições da pista.

**Métodos**:
- `__init__`: Inicializa uma corrida com os carros participantes.
- `run_race`: Simula a corrida completa, calculando os tempos de volta para cada carro e aplicando as regras de pit stops.

### `championship`

**Descrição**: Coordena a realização de várias corridas para formar um campeonato completo.

**Parâmetros**:
- `cars`: Lista de carros participantes no campeonato.
- `num_races`: Número de corridas no campeonato.

**Retorna**:
- Resultados do campeonato, contagem de vitórias e pontuação total de cada carro.

### `analyze_results`

**Descrição**: Analisa os resultados do campeonato para calcular a probabilidade de vitória de cada carro.

**Parâmetros**:
- `championship_results`: Resultados de todas as corridas do campeonato.
- `wins_count`: Contagem de vitórias de cada carro.
- `cars`: Carros participantes.

**Retorna**:
- Probabilidades de vitória para cada carro.

### `main`

**Descrição**: Função principal que inicializa os carros, executa o campeonato e visualiza os resultados.

## Funcionalidades Adicionais e Otimizações

- **Desgaste de Pneus e Combustível**: lógica onde o desgaste dos pneus e o consumo de combustível afetam progressivamente a performance dos carros ao longo das voltas.
- **Condições Meteorológicas Dinâmicas**: condições da pista mudam durante a corrida, influenciando a escolha de pneus e estratégias.
- **Pit Stops**: pit stops para troca de pneus ou reabastecimento.
- **Falhas Mecânicas Aleatórias**: chance de falhas mecânicas baseadas na confiabilidade do carro.
- **Penalidades**: penalidades para infrações de corrida como excesso de velocidade nos boxes ou saídas de pista.
