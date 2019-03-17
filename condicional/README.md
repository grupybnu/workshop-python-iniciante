# Condicionais
A Tomada de Decisão é composta por uma expressão a ser avaliada e o que deve acontecer caso a expressão seja verdadeira ou então, caso a expressão seja falsa. Sintaxe:

```
if <condição dada por operador booleano>:
    <o que tenho que fazer, caso a condição seja satisfeita> (caso a condição anterior não seja satisfeita, tenho mais uma condição para verificar)
elif <condição dada por operador booleano>:
    <o que tenho que fazer se a segunda condição for satisfeita>
else:
    <o que tenho que fazer, caso nenhuma das condições acima sejam satisfeitas>
```

Exemplos:
```python
def soma(a, b):
    return a + b

soma(1,2)

def soma_1_mais_2():
    return 1 + 2

soma_1_mais_2()
```