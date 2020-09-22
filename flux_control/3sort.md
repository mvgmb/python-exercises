# 3 Numeros em Ordem Crescente

## Descrição

Faça um programa que recebe 3 números inteiros e os imprima em ordem crescente.

## Input

03 números inteiros.

## Output

Os 03 números recebidos impressos em ordem crescente.

## Exemplos

```python
a = 555
b = 777
c = 666

# your code here

""" expected output:
555
666
777
"""
```

<details>
    <summary>Resposta</summary>
<p>

```python
a = 555
b = 777
c = 666

if (a > b):
    a, b = b, a

if (b > c):
    b, c = c, b

if (a > b):
    a, b = b, a

print(a, b, c)
```

</p>
</details>
