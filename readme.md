# Ponderada Prog 1 parte 1

### Segue o código para fazer a luz do arduíno piscar juntamente das imagens/vídeos na pasta "Assets"

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

