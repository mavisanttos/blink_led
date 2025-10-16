# Blink Led Interno

## Parte 1 – Blink LED Interno (Arduino)

Este projeto realiza o “blink” do LED interno do Arduino, fazendo com que ele acenda por 1 segundo (1000 milissegundos), apague por 1 segundo (1000 milissegundos) e repita esse ciclo continuamente — criando o efeito de uma luz piscando.

---

### Funcionamento

O código faz o LED interno do Arduino:

- Acender por um tempo determinado (1000 milissegundos).

- Apagar e aguardar outro tempo (1000 milissegundos).

- Repetir o processo em loop infinito.

---

### Código Utilizado
```c
// o setup funciona apenas uma vez ao ligar ou resetar a placa
void setup() { // declaração da função setup, tudo que estiver dentro de {} é executado uma vez no início
  pinMode(LED_BUILTIN, OUTPUT); // configura o pino do LED como saída
}

// a função loop é executado repetidamente enquanto a placa estiver ligada
void loop() { // declaração da função loop, tudo que estiver dentro de {} é executado em ciclo infinito
  digitalWrite(LED_BUILTIN, HIGH);  // envia tensão para o pino e faz o LED acender (estado lógico: HIGH)
  delay(1000);                      // pausa a execução por 1 segundo (1000 milissegundos) enquanto o LED permanece aceso
  digitalWrite(LED_BUILTIN, LOW);   // faz o LED desligar (estado lógico: LOW)
  delay(1000);                      // pausa a execução por 1 segundo (1000 milissegundos) enquanto o LED permanece apagado
} // fecha a função loop, a partir daqui o arduino volta e repete a função
```
---

### Evidências

#### Screenshot do código na Arduino IDE

#### Foto do Arduino conectado e LED interno aceso

#### Vídeo demonstrando o LED piscando

