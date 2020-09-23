# Invertido

## Descrição

Seu objetivo é gerar o invertido de um número de 3 algarismos.

## Input

Consiste de um número inteiro positivo de 3 algarismos.

## Output

Consiste de um número inteiro dado na entrada com a ordem dos algarismos invertida.

## Exemplos

```python
num = 123

# your code here

""" expected output:
321
"""
```

<details>
    <summary>Resposta 1</summary>
<p>

```python
num = 123
inv_num = 0

tail = int(num % 10)
inv_num = inv_num * 10 + tail
num = int(num / 10)

tail = int(num % 10)
inv_num = inv_num * 10 + tail
num = int(num / 10)

tail = int(num % 10)
inv_num = inv_num * 10 + tail
num = int(num / 10)

print(inv_num)
```

</p>
</details>

<details>
    <summary>Resposta 2</summary>
<p>

```python
num = str(123)

lista = []
for i in range(len(num)):
    lista.insert(i, num[i])
    
reversedstring = ''.join(reversed(lista))
print(int(reversedstring))
```

</p>
</details>


