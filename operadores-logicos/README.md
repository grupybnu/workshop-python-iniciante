# Operadores lógicos

Utilizamos quando queremos ter respostas lógicas, isto é, que retornam True ou False (verdadeiro/falso):

- Maior que: >
- Menor que: <
- Maior ou igual a: >=
- Menor ou igual a: <=
- Idêntico: ==
- Diferente de: !=
- Não: not
- E: and (exige que todas as condições sejam satisfeitas)
- Ou: or (apenas uma das condições precisa ser satisfeita)

Exemplos:
```python
a = 2
b = 3
a > b

b > a

a == b

a != b

a > b and b > a

a > b or b > a

not (a != b) ==False
```