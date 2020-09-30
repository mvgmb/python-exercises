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
bills = [100, 50, 20, 10, 5, 2, 1, 0.5, 0.25, 0.10, 0.05, 0.01]
num = 576.73

count = 0
for bill in bills:
    count = int(num / bill)
    print(count, "x R$", "{:.2f}".format(bill))
    num -= count * bill
```

</p>
</details>
