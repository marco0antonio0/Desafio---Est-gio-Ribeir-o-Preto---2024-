
**1 - Observe o trecho de código abaixo:**

int INDICE = 13, SOMA = 0, K = 0;

enquanto K < INDICE faça

{

K = K + 1;

SOMA = SOMA + K;

}

imprimir(SOMA);

Ao final do processamento, qual será o valor da variável SOMA?

```python
INDICE = 13
SOMA = 0
K = 0

while K < INDICE:
    K = K + 1
    SOMA = SOMA + K

print(SOMA)

```
**2 - Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.**
**IMPORTANTE:**

**RES:**
```python
# trecho em python
def fibonacci(n):
    sequence = [0, 1]
    while len(sequence) < n:
        next_number = sequence[-1] + sequence[-2]
        sequence.append(next_number)
    return sequence

def buscarDado(entrada_do_dado,result):
    res = False
    for i in result:
        if i == entrada_do_dado:
            res = True

n = 10
result = fibonacci(n)
print('sequencia de fibonacci:\n',result)

entada_de_dado = 11
saida = buscarDado(entada_de_dado,result)
if saida:
  print(f'dado {entada_de_dado} encontrado na sequencia')
else:
  print(f'dado {entada_de_dado} não encontrado na sequencia')
  


```
**RES:**
sequencia de fibonacci:

 [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]

dado 11 não encontrado na sequencia

**3 - Descubra a lógica e complete o próximo elemento:**
a) 1, 3, 5, 7, ___

b) 2, 4, 8, 16, 32, 64, ____

c) 0, 1, 4, 9, 16, 25, 36, ____

d) 4, 16, 36, 64, ____

e) 1, 1, 2, 3, 5, 8, ____

f) 2,10, 12, 16, 17, 18, 19, ____

**RES:**

a) 1, 3, 5, 7, 9

b) 2, 4, 8, 16, 32, 64, 128

c) 0, 1, 4, 9, 16, 25, 36, 49

d) 4, 16, 36, 64, 100

e) 1, 1, 2, 3, 5, 8, 13

f) 2, 10, 12, 16, 17, 18, 19, 20


**4 - Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.**
**Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?**

**RES:**

Para descobrir qual interruptor controla cada lâmpada com apenas duas idas até uma das salas das lâmpadas, você pode seguir este procedimento:

Primeira ida:

Ligue o primeiro interruptor e espere alguns minutos. Desligue o primeiro interruptor e ligue o segundo interruptor. Segunda ida:

Entre na sala. Se uma lâmpada estiver acesa, ela está conectada ao segundo interruptor. Se a lâmpada estiver desligada e estiver quente, ela está conectada ao primeiro interruptor. Se a lâmpada estiver desligada e não estiver quente, ela está conectada ao terceiro interruptor.

**5 - Escreva um programa que inverta os caracteres de um string.**
IMPORTANTE:

a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;

b) Evite usar funções prontas, como, por exemplo, reverse;

**RES:**


```
# trecho em python
def inverter_string(s):
    inverted = ''
    for i in range(len(s) - 1, -1, -1):
        inverted += s[i]
    return inverted

# Exemplo de uso

string = input("Digite uma string: ")
print("String original:", string)
print("String invertida:", inverter_string(string))

```
**RES:**
Digite uma string: ola

String original: ola
String invertida: alo
