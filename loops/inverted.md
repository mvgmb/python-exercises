# Invertido

## Descrição

Seu objetivo é gerar o invertido de um número **_usando laços_**.

## Input

Consiste de um número inteiro positivo.

## Output

Consiste de um número inteiro dado na entrada com a ordem dos algarismos invertida.

## Exemplos

```python
num = 12345

# your code here

""" expected output:
54321
"""
```

<details>
    <summary>Resposta</summary>
<p>

```python
num = 12345

inv_num = 0
while(num != 0):
	tail = int(num % 10)
	inv_num = inv_num * 10 + tail
	num = int(num / 10)

print(inv_num)
```

</p>
</details>
