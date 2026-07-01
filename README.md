# Pulseira-de-Triagem - Circuitos-Digitais

Nesse projeto da matéria de circuitos de digitais da UNIFESP, Universidade Federal de São Paulo, decidimos realizar o circuito de uma pulseira que realiza uma triagem médica baseada no protocolo de Manchester.

## Como utilizar

1. Instale a versão **4.3.0** do WiRedPanda.
2. Abra o arquivo `Circuito.panda`.

Esse arquivo contém o circuito principal, que recebe entradas de 3 sensores:

- **Sensor de BPM** — possui duas opções de entrada:
  - **Contador automático**: simula o funcionamento real do sensor, percorrendo as faixas de 45–55 bpm e 95–110 bpm.
  - **Valor manual**: o usuário insere o valor desejado através de uma entrada de 7 bits, cobrindo até 127 bpm.
  ![Circuito do sensor de BPM](https://github.com/gpombotky/Triagem-Circuitos-Digitais/blob/main/circuitos-digitais/imagens/Captura%20de%20Tela%202026-06-30%20a%CC%80s%2021.56.41.png)

- **Sensor de SpO2** — também possui duas opções de entrada:
  - **Contador automático**: simula os possíveis resultados da fração usada para calcular a porcentagem de O2 no sangue, contando de 0 a 6.
  - **Valor manual**: o usuário insere um valor X em 3 bits. Esse valor é convertido na porcentagem de SpO2 pela fórmula `110 − 5X`, cobrindo a faixa de 80% (X=6) a 110% (X=0).
  ![Circuito do sensor de SpO2](https://github.com/gpombotky/Triagem-Circuitos-Digitais/blob/main/circuitos-digitais/imagens/Captura%20de%20Tela%202026-06-30%20a%CC%80s%2022.02.38.png)

- **Sensor de temperatura** — recebe uma entrada manual de 6 bits, cobrindo a faixa de 0°C a 64°C.
  - ![Circuito do sensor de Temperatura](https://github.com/gpombotky/Triagem-Circuitos-Digitais/blob/main/circuitos-digitais/imagens/Captura%20de%20Tela%202026-06-30%20a%CC%80s%2022.01.10.png)

A combinação dos valores dos três sensores determina a cor do LED de saída, indicando o nível de risco do paciente.
