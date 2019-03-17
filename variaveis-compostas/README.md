# Variáveis Compostas

São compostas por mais de um valor "simples" (mais de um número, mais de uma string) ou "compostas" (lista, tupla, dict, etc...).

## Seus tipos são:
- [list](#list)
- [tuple](#tuple)
- [dict](#dict)
- [set](#set)

## list
Permitem armazenar várias informações em uma mesma variável. É uma estrutura de dados que pode conter itens. No Python nos é fornecido um objeto do tipo list e todos elementos que estiverem delimitados por colchetes, será interpretado pela linguagem, como um conjunto de itens pertencentes a uma lista. Sintaxe:

```
<variável> = [info1, info2, info3]
```

Exemplos:
```python
a = ['String', 9, True]
a

b = [['Nome', 99999], True]
b

type(b)
```

### Acessando itens da lista
Índice em uma lista: número que indica a posição de cada caractere na string. O número será 0 (zero) para o primeiro caractere na string, 1 para o segundo, 2 para o terceiro, etc. Sintaxe:

```
<lista>[número]
```

Exemplos:
```python
['a', 2, True, [1], 'GruPy Blumenau']
```

'a' | 2 | True | [1] | 'GruPy Blumenau'
----|---|------|-----|-----------------
  0 | 1 |  2   |  3  |       4

```python
a = ['a', 2, True, [1], 'GruPy Blumenau']

a[0]

a[3]

a[2]
```

### Partes de uma lista (slicing)
Retorna parte da lista, começando pelo primeiro índice e terminando no anterior ao segundo. Sintaxe:

```
<lista>[índice1:índice2]
```

**OBS: Quando omitimos um índice, é mostrado o caractere do extremo correspondente**

Exemplos:
```python
['a', 2, True, [1], 'GruPy Blumenau']
```

'a' | 2 | True | [1] | 'GruPy Blumenau'
----|---|------|-----|-----------------
  0 | 1 |  2   |  3  |       4

```python
a = ['a', 2, True, [1], 'GruPy Blumenau']

a[0:2]

a[2:]

a[:3]
```

### Incremento de fatia (slicing)
Permite resgatar índices alternados, e até mesmo inverter uma lista. Sintaxe:

```
<lista>[índice1:índice2:<incremento>]
```
Exemplos:
```python
['a', 2, True, [1], 'GruPy', 1, 2]
```

'a' | 2 | True | [1] | 'GruPy' | 1 | 2
----|---|------|-----|---------|---|---
  0 | 1 |  2   |  3  |   4     | 5 | 6

```python
a = ['a', 2, True, [1], 'GruPy', 1, 2]

a[::2]

a[::-1]

a[5:0:-2]
```

### Tamanho da sua Lista
Para saber o tamanho da sua lista, basta pedir para o Python a partir da comando "len". Sintaxe:

```
len(<lista>)
```

Exemplos:
```python
a = [1, 2, 3]
len(a)
```

### Adicionando itens a minha lista (<list>.append(VALOR))
Existem duas formas de fazer isso:
- "concatenando" listas
- adicionado o item com a comando append.

Sintaxe:

```
<lista>.append(<item para adicionar>)

ou

<lista1> + <lista2>
```

Exemplos:
```python
a = [1, 2]

a.append(3)

a

b = [4, 5]

a + b
```

### Listas de Letras (vulgo strings)
O Python, como a maioria das linguagem, entende que a string é uma lista de letras, logo, você pode aplicar alguns comandos das listas em strings \o/

Exemplos:
```python
a = 'Pyladies'

a[:2]

a[0:5:2]

a[::-1]

a[5:0:-2]

len(a)
```

### Transformando uma lista em uma string
Join: gruda os elementos de uma sequência de strings, usando uma string fornecida, que será usada para "dividir os itens da lista". Sintaxe:

```
'string'.join(<lista>)
```

Exemplos:
```python
a = ['banana', 'limão', 'maçã']

','.join(a)
```
