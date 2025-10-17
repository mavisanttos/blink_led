# Blink Led Interno

## Parte 1 – Blink LED Interno (Arduino)

&emsp; Este projeto realiza o “blink” do LED interno do Arduino, fazendo com que ele acenda por 1 segundo (1000 milissegundos), apague por 1 segundo (1000 milissegundos) e repita esse ciclo continuamente — criando o efeito de uma luz piscando.

---

### Funcionamento

O código faz o LED interno do Arduino:

- Acender por um tempo determinado (1000 milissegundos).

- Apagar e aguardar outro tempo (1000 milissegundos).

- Repetir o processo em loop infinito.

---

### Componentes utilizados

| **Componente**  | **Descrição**                                                                           |
| --------------- | --------------------------------------------------------------------------------------- |
| **Arduino UNO** | Placa principal utilizada para o controle do circuito e execução do código.             |
| **Cabo USB**    | Responsável pela alimentação e comunicação entre o Arduino e o computador.              |
| **LED**         | Componente emissor de luz utilizado para demonstrar o piscar.                           |
| **Arduino IDE** | Ambiente de desenvolvimento usado para escrever, compilar e enviar o código ao Arduino. |

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

[Assista ao vídeo no Google Drive](https://drive.google.com/file/d/1QQKh9uTJVaOuTOY_MhBF_BXGAz6fiGJa/view?usp=sharing)


<em>Demonstração em vídeo do Arduino executando o código “Blink”, com o LED interno acendendo e apagando em intervalos regulares.</em>
</div>

---

## Parte 2 – Simulando Blink Externo (Arduino + Tinkercad)

&emsp; Esta parte do projeto tem como objetivo simular um circuito de pisca-pisca (Blink) utilizando o Arduino UNO no ambiente de simulação Tinkercad.
A montagem deve conter um LED externo (off-board) conectado a um protoboard, resistor e ligações elétricas adequadas.

&emsp; Ao executar a simulação (clicando em “Play” no Tinkercad), o LED deve acender e apagar de forma contínua, seguindo o tempo definido no código.

---

### Funcionamento

&emsp; O código desenvolvido envia comandos elétricos para o pino digital configurado como saída (OUTPUT). A lógica é semelhante ao Blink interno, mas agora o LED está conectado externamente a uma das portas do Arduino.

&emsp; Etapas de funcionamento:

- Define-se o pino do LED (porta 13, que é a padrão para o exemplo de “Blink” no Arduino) como saída.

- O programa envia sinal HIGH (ligado) — o LED acende.

- Aguarda um tempo definido (1000 milissegundos).

- Envia sinal LOW (desligado) — o LED apaga.

- Aguarda novamente (1000 milissegundos).

- O processo se repete em loop infinito.

---

### Código utilizado

```c
void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000);
}
```

---

### Componentes Utilizados

| Componente              | Quantidade | Função                                         |
| ----------------------- | ---------- | ---------------------------------------------- |
| Arduino UNO             | 1          | Controlador principal do circuito              |
| Protoboard              | 1          | Base para montagem dos componentes             |
| LED (off-board)         | 1          | Indica visualmente o funcionamento do circuito |
| Resistor (1000Ω) | 1          | Limita a corrente elétrica do LED              |
| Jumpers                 | 2    | Conectam os pinos do Arduino ao protoboard     |

---

### Simulação no Tinkercad

Nesta simulação, o circuito é montado com Arduino UNO, protoboard, LED externo (off-board), resistor e jumpers.
As conexões seguem o padrão:

- Jumper vermelho: conecta o pino digital 13 do Arduino à perna positiva do LED (anodo).

- Resistor (1000Ω): conectado entre a perna negativa do LED (cátodo) e a linha de terra do protoboard.

- Jumper preto: conecta o GND do Arduino à linha de terra do protoboard.

---

### Evidências

 Montagem no Tinkercad

Captura de tela mostrando o circuito montado com o Arduino, protoboard, resistor e LED.


 Código no Tinkercad

Screenshot do código desenvolvido no ambiente de simulação.


 Simulação em funcionamento

GIF ou vídeo mostrando o LED piscando alternadamente.