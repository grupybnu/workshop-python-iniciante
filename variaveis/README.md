# Variáveis

Variáveis são como gavetas nomeadas para o computador, onde ele guarda as informações que você dá a ele.

E como é "nomeada", você não precisa saber onde está a gaveta, só precisa saber o nome dela.

Quando você precisa buscar uma informação, você diz o nome da gaveta e o computador vai lá e "abre" esta gaveta.

Abra o seu terminal iterativo python e vamos fazer declarar a nossa primeira variável.

```python
minha_primeira_variavel = "Olá Variáveis!!!"

print(minha_primeira_variavel)
```

Mas como tudo na vida... Tem regras!

## Regras

- Podem ser usados números, letras ou _
- Nunca devem começar com um algarismo

E tem palavras reservadas que o Python usa para entender o que queremos que ele faça, como aquele "print" que demos.

Para conseguirmos nos comunicar com o Python, não podemos dizer que uma dessas palavras reservas é uma gaveta(variável), senão, ao invés do computador "printar" ele vai abrir uma gaveta (mostra o valor da variável).


## Tipos de variáveis simples

Para saber como organizar essas variáveis, o Python tem tipos de variáveis:

- Numéricos: Armazena números. São: inteiros (int), de ponto flutuante (float)
- Letras: Armazena caracteres (qualquer um do teclado). São strings (string)
- Lógicos: Armazena verdadeiro ou falso. São: booleanos (bool)

### Numéricos

Tipo inteiro (int): números inteiros, sem ponto da casa decimal.
```python
a = 2
b = 4
c = 0
```

Tipo ponto flutuante (float): números que aparece o ponto da casa
decimal.
```python
d = 2.0
e = 4.5
f = 0.0
```

### Letras

String (str): compreende todos os caracteres dentro de aspas (simples ou duplas)
```python
j = "2"
k = "2.0"
l = "12@#nikukyu"
m = "ççççççç"
```

### Lógicos

Booleanos (bool): compreende respostas do tipo True ou False (Verdadeiro ou
Falso)
```python
n = True
o = False
```

## Descobrindo o tipo de variáveis no Python

Existe uma forma de pedir para o Python te dizer qual o tipo do valor:
Sintaxe:
```python
type(<nome_da_variavel>)
```

Exemplo:
```python
m = False
type(m)
<type "bool">
```

## Transformando tipos de variáveis no Python

Para transformar um tipo de variável em outro é usando os comandos:
- int()
- float()
- bool()
- str()

Exemplos:
```python
a = 2
type(a)
<class "int">

d = str(a)
d
b = float(a)
type(b)
<class "float">

e = int(d)
e
type(e)
<class "int">
```

## Exercícios

1. Teste algumas variáveis definidas anteriormente.
2. Tente definir m = true
- O que acontece? Por que dava certo quando era True?
- Tente m = "true" e verifique o tipo de m.
- Qual sua teoria para explicar o que aconteceu?

Perdeu alguma variável pelo caminho?
```python
a = 2
b = 4
c = 0
d = 2.0
e = 4.5
f = 0.0
g = "2"
h = "2.0"
i = "12@#nikukyu"
j = "ççççç"
k = True
l = False
```