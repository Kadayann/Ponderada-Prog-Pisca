

# Ponderada Prog 1

Link com drive contendo fotos e vídeos dos projetos físicos e no simulador: [Acesse aqui](https://drive.google.com/drive/folders/1rTKCDDVNUneCG47Ih89xCAuCTLv79lyE?usp=drive_link)

## Parte 1

### Código que faz o LED do Arduino piscar.

```cpp
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
```

### Foto da parte 1 (caso não carregue no github, o link do drive está no começo do repositório)


<img src="https://github.com/user-attachments/assets/5f92f6aa-58c0-46b3-a9bb-79f26d903d64" width="700" height="850" alt="Descrição da imagem">




<img src="https://github.com/user-attachments/assets/bd142603-e99d-4673-ba84-79db35cbfe6e" width="400" height="550" alt="Descrição da imagem">


## Parte 2

### Após fazer a primeira parte ligando o LED integrado do Arduino fiz a segunda parte com LEDs adicionais e uma fiação mais complexa, envolvendo os cabos "jumpcable", um vermelho e um azul acompanhado de resistores, esse foi o código para ambos LEDs acenderem de forma intercalada simulando uma sirene.


```cpp
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
```

### Fotos da parte 2

<img src="https://github.com/user-attachments/assets/b53a05f8-a467-4b0c-a15f-f22f940919e2" width="700" height="850" alt="Descrição da imagem">

<img src="https://github.com/user-attachments/assets/7472cc71-ac75-4564-a157-a42e9d828d49" width="400" height="550" alt="Descrição da imagem">

<img src="https://github.com/user-attachments/assets/031b55f0-f614-43e2-b2fd-ae6e0967d91f" width="400" height="550" alt="Captura de tela 2025-10-17 093820">




### Processo de pensamento

Após realizar o circuito no simulador e confirmar com o código e a elétrica que funcionou, decidi partir para o modelo físico, inicialmente com apenas o led azul piscando e acendendo. Para ir além, eu decidi adicionar mais um led, só que vermelho, e fazê-los piscar intercaladamente como um giroflex de um carro policial. Inicialmente o circuito não estava funcionando, mas eu estava invertendo os polos dos LEDs e encaixando os resistores de forma incorreta, em linhas diferentes e não conectadas, porém após pesquisa consegui fazer funcionar, o mesmo ocorreu com o código, onde ambos os LEDs estavam piscando ao mesmo tempo, mas coordenando o delay entre eles consegui fazer funcionar.

# Importante

### Os vídeos dos projetos funcionando não foram anexados nesse repositório por conta do tamanho dos arquivos, eles se encontram na pasta do drive.




