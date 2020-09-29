# Notas e Moedas

## Descrição

Receba um valor de ponto flutuante com duas casas decimais. Este valor representa um valor monetário. A seguir, calcule o menor número de notas e moedas possíveis no qual o valor pode ser decomposto. As notas consideradas são de 100, 50, 20, 10, 5, 2. As moedas possíveis são de 1, 0.50, 0.25, 0.10, 0.05 e 0.01. A seguir mostre a relação de notas necessárias.

## Input

O arquivo de entrada contém um valor de ponto flutuante N com duas casas decimais.

## Output

Imprima a quantidade mínima de notas e moedas necessárias para trocar o valor inicial, conforme exemplo fornecido.

## Exemplos

```python
num = 576.73

# your code here

""" expected output:
5 x R$ 100.00
1 x R$ 50.00
1 x R$ 20.00
0 x R$ 10.00
1 x R$ 5.00
0 x R$ 2.00
1 x R$ 1.00
1 x R$ 0.50
0 x R$ 0.25
2 x R$ 0.10
0 x R$ 0.05
3 x R$ 0.01
"""
```

<details>
    <summary>Resposta 1</summary>
<p>

```python
num = 576.73

count = 0

# bills
count = int(num / 100)
print(count, "x R$ 100.00")
num -= count * 100

count = int(num / 50)
print(count, "x R$ 50.00")
num -= count * 50

count = int(num / 20)
print(count, "x R$ 20.00")
num -= count * 20

count = int(num / 10)
print(count, "x R$ 10.00")
num -= count * 10

count = int(num / 5)
print(count, "x R$ 5.00")
num -= count * 5

count = int(num / 2)
print(count, "x R$ 2.00")
num -= count * 2

count = int(num)
print(count, "x R$ 1.00")
num -= count

# coins
num *= 100

count = int(num / 50)
print(count, "x R$ 0.50")
num -= count * 50

count = int(num / 25)
print(count, "x R$ 0.25")
num -= count * 25

count = int(num / 10)
print(count, "x R$ 0.10")
num -= count * 10

count = int(num / 5)
print(count, "x R$ 0.05")
num -= count * 5

count = int(num)
print(count, "x R$ 0.01")
num -= count
```

</p>
</details>

<details>
    <summary>Resposta 2</summary>
<p>

```python
num = float(576.73)

i = 0 
while num > 100:
    num = num - 100
    i+=1
print(i, "x R$ 100.00")

i = 0
while num > 50:
    num = num - 50
    i+=1
print(i, "x R$ 50.00")

i = 0
while num > 20:
    num = num - 20
    i+=1
print(i, "x R$ 20.00")

i = 0
while num > 10:
    num = num - 10
    i+=1
print(i, "x R$ 10.00")

i = 0
while num > 5:
    num = num - 5
    i+=1
print(i, "x R$ 5.00")

i = 0
while num > 2:
    num = num - 2
    i+=1
print(i, "x R$ 2.00")

i = 0
while num > 1:
    num = num - 1
    i+=1
print(i, "x R$ 1.00")

i = 0
while num > 0.5:
    num = num - 0.5
    i+=1
print(i, "x R$ 0.50")

i = 0
while num > 0.25:
    num = num - 0.25
    i+=1
print(i, "x R$ 0.25")

i = 0
while num > 0.10:
    num = num - 0.10
    i+=1
print(i, "x R$ 0.10")

i = 0
while num > 0.05:
    num = num - 0.05
    i+=1
print(i, "x R$ 0.05")

i = 0
while num > 0.01:
    num = num - 0.01
    i+=1
print(i, "x R$ 0.01")
```

</p>
</details>