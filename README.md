# Sistema de Irrigação Automática com Arduino

## Descrição
Este projeto implementa um sistema de irrigação automatizado utilizando Arduino Uno. O sistema mede a umidade do solo, a luminosidade ambiente e a temperatura, acionando uma bomba d'água apenas quando necessário. LEDs indicam o estado da leitura, irrigação, excesso de umidade e erros. Um botão permite ligar e desligar o sistema manualmente.

## Funcionalidades
- Monitoramento de umidade do solo com sensor capacitivo v1.2 (ou sensor de duas hastes no protótipo).
- Monitoramento de luminosidade e temperatura ambiente.
- Acionamento automático de bomba de água via relé (ativo LOW).
- LEDs indicadores:
  - **Amarelo**: leitura em andamento.
  - **Verde**: irrigação ativa.
  - **Azul**: solo ideal ou úmido demais (não irrigar).
  - **Vermelho**: erro na leitura.
- Botão para ligar/desligar o sistema.
- Exibição de valores no Serial Monitor.

## Materiais Utilizados
- Arduino Uno R3
- Sensor de umidade do solo capacitivo v1.2
- Sensor de luminosidade (LDR ou módulo digital)
- Sensor de temperatura (DS18B20)
- Bomba de aquário 3-6V
- Módulo relé 5V
- LEDs (amarelo, azul, verde, vermelho)
- Resistores e jumpers
- Protoboard
- Fonte de alimentação 9V / 1A

## Instalação
1. Instale o [Arduino IDE](https://www.arduino.cc/en/software).
2. Instale as bibliotecas necessárias:
   - `OneWire`
   - `DallasTemperature`
3. Conecte os sensores e LEDs aos pinos especificados no código.
4. Faça upload do código para o Arduino.

## Uso
- Pressione o botão para ligar o sistema. O LED amarelo indicará a leitura do sensor.
- O LED verde acenderá quando a bomba estiver irrigando.
- O LED azul indica que a umidade está dentro da faixa ideal ou excesso de água.
- O LED vermelho indica erro na leitura do sensor.
- Os valores podem ser acompanhados pelo Serial Monitor.

## Código
O código principal está no arquivo `Irrigacao_Automatica.ino`.

## Observações
- Ajuste os limites de umidade (`limiteSeco` e `limiteUmido`) conforme a necessidade da planta ou do solo.
- Para o DS18B20, utilize resistor de pull-up de 4.7kΩ entre VCC e sinal.
