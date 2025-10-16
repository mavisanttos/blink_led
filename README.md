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

<div align="center">
<figcaption><strong>Screenshot do código na Arduino IDE</strong></figcaption>
<br>
<img src="assets/codigo_arduino.png" width="100%">
<br>
<em>Captura de tela mostrando o código desenvolvido na Arduino IDE, responsável por fazer o LED interno piscar em intervalos de 1 segundo.</em>
</div>

<br>

<div align="center">
<figcaption><strong>Foto do Arduino com LED aceso</strong></figcaption>
<br>
<img src="assets/arduino_conectado.jpg" width="100%">
<br>
<em>Fotografia do Arduino conectado ao computador, com o LED interno aceso, comprovando o funcionamento do circuito e a execução correta do código.</em>
</div>

<br>

<div align="center">
<figcaption><strong>Vídeo demonstrando o LED piscando</strong></figcaption>
<br>

[Clique aqui para assistir ao vídeo do LED piscando](assets/video_arduino.mp4)

<br>
<em>Demonstração em vídeo do Arduino executando o código “Blink”, com o LED interno acendendo e apagando em intervalos regulares.</em>
</div>