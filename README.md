# Alimentador de Petiscos com Sensor Ultrassônico

Este projeto consiste em um alimentador automático de petiscos acionado por um sensor de distância ultrassônico. Quando o sensor detecta que algo (possivelmente um animal de estimação) está a menos de 20 cm, ele aciona um servo motor para abrir e fechar um compartimento de petiscos.

## Descrição
- **Sensor Ultrassônico**: Utilizado para medir a distância do objeto/alvo.  
- **Servo Motor**: Controla a abertura e o fechamento do compartimento.  
- **Arduino**: Faz a leitura do sensor e envia comandos para o servo.

## Funcionamento
1. O Arduino envia um pulso pelo pino TRIG do sensor.  
2. O sensor retorna um pulso pelo pino ECHO com duração proporcional à distância do objeto.  
3. O Arduino converte a duração do pulso em centímetros.  
4. Se a distância for inferior a 20 cm, o servo motor se move para liberar o petisco e retorna à posição inicial.

## Requisitos de Hardware
- 1 x Arduino (UNO, Nano ou outro compatível)  
- 1 x Sensor Ultrassônico (HC-SR04 ou similar)  
- 1 x Servo Motor (ex.: SG90 ou MG90S)  
- Jumpers e fios para conexão  
- Uma fonte de alimentação suficiente para o servo (caso necessário)  
- Compartimento de armazenamento de petiscos

## Conexões
- **Sensor Ultrassônico**  
  - VCC -> 5V  
  - GND -> GND  
  - TRIG -> Pino 3 (Arduino)  
  - ECHO -> Pino 4 (Arduino)  

- **Servo**  
  - VCC -> 5V  
  - GND -> GND  
  - Sinal -> Pino 2 (Arduino)

## Como Usar
1. Faça todas as conexões conforme indicado.  
2. Carregue o código `alimentador_petiscos.ino` na placa Arduino.  
3. (Opcional) Abra o Serial Monitor para depuração (caso queira adicionar `Serial.print` ao código).  
4. Garanta que o compartimento de petiscos esteja corretamente posicionado.  
5. Observe o movimento do servo quando um objeto estiver a menos de 20 cm do sensor.

## Adicionando Mais Scripts
- Crie uma nova pasta ou utilize a pasta existente para adicionar novos códigos `.ino` e bibliotecas.  
- Mantenha o `README.md` atualizado com uma breve descrição de cada novo script/projeto adicionado.

## Melhorias Futuras
- Adicionar um display LCD ou OLED para mostrar mensagens ou a distância medida.  
- Incluir um módulo Wi-Fi ou Bluetooth para acionar remotamente ou enviar notificações ao smartphone.  
- Controlar a quantidade de petiscos liberada, regulando melhor o ângulo ou a duração do servo.  

---

**Autor:**  
[Diego Maciel Geronimo]  
Data de Criação: [2019-01-28]

**Licença:**  
Este projeto é livre para uso pessoal e educacional. Verifique as licenças das bibliotecas utilizadas para mais detalhes.

> **Observação**: Se o servo apresentar falhas por falta de energia, utilize uma fonte externa de 5V que compartilhe o mesmo GND do Arduino.
