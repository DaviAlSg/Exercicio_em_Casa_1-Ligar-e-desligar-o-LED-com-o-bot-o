# Exercicio_em_Casa_1-Ligar-e-desligar-o-LED-com-o-bot-o
-
-
# Arduino feito no Tinkercard 
-
-
![Editing Components (4)](https://github.com/user-attachments/assets/7684322d-1ef4-4af9-8665-ef2c84c41e1c)
-
-Conecte um botão entre o pino de 5V e o pino digital D2 do Arduino, com um resistor de 10kΩ ao GND. O ânodo do LED deve ser ligado ao pino D12, e o cátodo a um resistor de 220Ω, que se conecta ao GND.
Conecte os pinos de 5V e GND do Arduino à protoboard. Este circuito serve para acender o LED quando o botão é pressionado.
-
# Materiais
1 Fio de 10 k ohm,
1 Fio de 220 ohm,
1 Led,
1 Protobord,
1 Botão,

# Código
-
# Código
const int buttonPin = 2;
const int ledPin = 13;


// variables will change:
int buttonState = 0;


void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}


void loop() {
  buttonState = digitalRead(buttonPin);
  if (buttonState == HIGH) {
    digitalWrite(ledPin,HIGH);
  } else {
    digitalWrite(ledPin,LOW);
  }
}
