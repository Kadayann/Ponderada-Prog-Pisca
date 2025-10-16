# Ponderada Prog 1 parte 1

### Código que faz a luz do arduíno piscar e imagens/vídeos do mesmo na pasta "Assets".

void setup() {
  // inicializa o pino digital LED_BUILTIN como uma saída.
  pinMode(LED_BUILTIN, OUTPUT);
}

// a função loop roda repetidamente para sempre
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // acende o LED (HIGH é o nível de voltagem alto)
  delay(4000);                      // espera 4 segundos
  digitalWrite(LED_BUILTIN, LOW);   // apaga o LED (colocando o nível de voltagem em LOW)
  delay(3000);                      // espera 3 segundos
}


# Ponderada Prog 1 parte 1

### Após fazer a primeira parte ligando o led integrado do arduíno fiz a segunda parte com LEDs adicionais e uma fiação mais complexa, envolvendo os cabos "jumpcable", um vermelho e um azul acompanhado de resistores, esse foi o código para ambos LEDs acenderem de forma intercalada simulando uma sirene.

void setup() {
  pinMode(2, OUTPUT); // LED vermelho
  pinMode(3, OUTPUT); // LED azul
}

void loop() {
  // Liga o vermelho e apaga o azul
  digitalWrite(2, HIGH);
  digitalWrite(3, LOW);
  delay(200);

  // Apaga ambos por um instante 
  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  delay(50);

  // Liga o azul e apaga o vermelho
  digitalWrite(2, LOW);
  digitalWrite(3, HIGH);
  delay(200);

  // Apaga ambos de novo
  digitalWrite(2, LOW);
  digitalWrite(3, LOW);
  delay(50);
}

