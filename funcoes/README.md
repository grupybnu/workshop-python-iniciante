# Funções
Funções são pedaços de código que servem para executar um procedimento muitas vezes, evitando que você tenha que reescrevê-lo mais de uma vez.

Uma funcionalidade importante é o fato que, caso precise realizar alguma alteração ou correção, ela vai ser feita neste pedaço de código e não em diversas partes do código. Sintaxe:

- Quando a função sempre faz a mesma coisa do mesmo jeito:
```
def <nome da função> ():
    <pedaço do código que você quer executar>
```

- Quando a função faz coisas dependendo do valor dos parâmetros:
```
def <nome da função> (<parâmetro(s)>):
    <pedaço do código que você quer executar>
    return (caso essa função retorne algum valo r)
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

## Funções nativas do Python

- [dir](#dir)
- [help](#help)
- [input](#input)

[Link da documentação completa do Python](https://docs.python.org/3/library/functions.html)

### dir
Lista todos os comandos válidos para a variável. Sintaxe:

```
dir(<variável>)
```

Exemplos:
```python
dir('string')

dir(1)

dir(dict)

dir([])
```

[:arrow_up: Voltar para menu "Funções nativas do Python"](#funções-nativas-do-python)

### help
Retorna a documentação do tipo ou objeto que estamos inspecionando.

```
help(<variável>)
```

Exemplos:
```python
a = 'string'
help(a)

help(dict)

help([])
```

[:arrow_up: Voltar para menu "Funções nativas do Python"](#funções-nativas-do-python)

### input
Para pegarmos o valor das variáveis pela tela, no Python, usamos o comando "input". Existem duas formas de pegar o valor da variável: pegando sempre como string ou "tipando" ela como um tipo de variável. Sintaxe:

```
<variável> = input(<"mensagem para o usuário entrar com o valor>")
ou
<variável> = <tipo da variável>(input(<"mensagem para o usuário entrar
com o valor>"))
```

Exemplos:
```python
input('Qual é o seu nome?')

idade = input('Qual é a sua idade?')
idade
type(idade)

idade = int(input('Qual é a sua idade?')) # transformando em inteiro
idade
type(idade)
```

[:arrow_up: Voltar para menu "Funções nativas do Python"](#funções-nativas-do-python)