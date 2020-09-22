# Pagamento IPVA

## Descrição

Todos os anos, os motoristas devem pagar ao Detran o IPVA (Imposto sobre a Propriedade de Veículos Automotores) e uma taxa de trânsito. Caso paguem o IPVA com antecedência, recebem um desconto de 5% apenas no valor desse imposto. Escreva um programa que receba como entrada o valor do IPVA e o valor da taxa de trânsito, e exiba o total a ser pago por um motorista que deseja quitar sua dívida cinco dias antes do prazo.

## Input

Dois valores reais, sendo o primeiro correspondente ao IPVA e o segundo correspondente à taxa de trânsito

## Output

Um valor real com apenas duas casas decimais

## Exemplos

```python
ipva = 100.00
trafficTax = 80.00

# your code here

""" expected output:
175.00
"""
```

<details>
    <summary>Resposta</summary>
<p>

```python
ipva = 100.00
trafficTax = 80.00

totalTax = ipva * 0.95 + trafficTax
formattedTotalTax = "{:.2f}".format(totalTax)

print(formattedTotalTax)
```

</p>
</details>
