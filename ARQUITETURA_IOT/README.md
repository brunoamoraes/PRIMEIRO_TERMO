# 📡 Arquitetura IoT: Guia de Aula
> **Foco:** Integração Hardware-Software e Comunicação

---

## 1. 🏗️ Visão Geral da Arquitetura
A arquitetura IoT básica tratada nesta aula segue o modelo de três camadas:
1.  **Percepção (Arduino):** Sensores e atuadores.
2.  **Rede/Processamento (Python/Gateway):** Tratamento de dados e conectividade.
3.  **Aplicação:** Dashboards e armazenamento em nuvem.

---

## 2. 🤖 O Ecossistema Arduino
O Arduino atua como nossa unidade de controle de borda (*Edge*).

### Principais Componentes:
*   **Microcontrolador:** ATmega328P (no caso do Uno).
*   **I/O:** Portas Digitais (0-13) e Analógicas (A0-A5).
*   **Comunicação:** Serial (UART), I2C e SPI.

---

## 3. 💻 Programação C++ (No Arduino)
O Arduino utiliza uma versão simplificada de C++. Todo código segue a estrutura base:

```cpp
// Definições de Pinos
const int LED_PIN = 13;

void setup() {
  // Executa uma vez ao ligar
  pinMode(LED_PIN, OUTPUT);
  Serial.begin(9600); // Inicia comunicação serial
}

void loop() {
  // Executa em loop infinito
  digitalWrite(LED_PIN, HIGH);
  Serial.println("Dado enviado do Sensor: 1");
  delay(1000);
  digitalWrite(LED_PIN, LOW);
  delay(1000);
}
```

---

## 4. 🐍 Programação Python (Integração)
No contexto de IoT, o Python é usado para ler os dados do Arduino via Serial e enviá-los para a nuvem ou bancos de dados.

### Exemplo de Script de Leitura (Biblioteca `pySerial`):
```python
import serial
import time

# Configuração da porta (ajuste o 'COM3' ou '/dev/ttyUSB0')
arduino = serial.Serial(port='COM3', baudrate=9600, timeout=.1)

def read_arduino():
    while True:
        data = arduino.readline().decode('utf-8').strip()
        if data:
            print(f"Recebido do Arduino: {data}")
        time.sleep(1)

if __name__ == "__main__":
    read_arduino()
```

---

## 5. 🛠️ Exercício Prático
1.  **Hardware:** Montar um sensor de temperatura no Arduino.
2.  **Firmware (C++):** Programar o Arduino para enviar o valor da temperatura via Serial a cada 2 segundos.
3.  **Software (Python):** Criar um script que receba esse valor e salve em um arquivo `.csv`.

---

## 📚 Referências e Links Úteis
*   [Documentação Oficial Arduino](https://arduino.cc)
*   [Documentação PySerial](https://readthedocs.io)
*   [ESP32 vs Arduino em Projetos IoT](https://espressif.com)
