# Operações com strings

## Transformando strings

### Concatenação
A concatenação é como se você "somasse" palavras.

Sintaxe:
"<string>" + "<string>"

Exemplos:
```python
'a' + 'b'
'Eu' + ' ' + 'amo'  + ' ' + 'Python!!!'
```

### "multiplicar" palavras

Sintaxe:
"<string>" * "<string>"

Exemplos:
```python
'k' * 6
'bla' * 3
```

### Uppercase:

Todas as letras de uma string em maiúscula (pode fazer com uma variável tipo string também). Sintaxe:

"<string>".upper()

ou

variavel_do_tipo_string.upper()

Exemplos:
```python
'minha string'.upper()

string = 'Essa é uma string'
string.upper()
```

### Lowercase
Todas as letras de uma string em minúscula (pode fazer com uma variável tipo string também). Sintaxe:

"<string>".lower()

ou

variavel_do_tipo_string.lower()

Exemplos:
```python
'minha string'.lower()

string = 'Essa é uma string'
string.lower()
```

### Capitalize
Transforma apenas a primeira em letra maiúscula (se for um número, ele não faz nada). Sintaxe:

"<string>".capitalize()

ou

variavel_do_tipo_string.capitalize()

Exemplos:
```python
'minha string'.capitalize()

string = 'Essa é uma string'
string.capitalize()

string_com_numero = 'Essa é uma string com o número 42'
string_com_numero.capitalize()
```

### Title
Coloca a primeira letra de cada palavra em maiúscula. Sintaxe:

"<string>".title()

ou

variavel_do_tipo_string.title()

Exemplos:
```python
'minha string'.title()

string = 'Essa é uma string'
string.title()
```

### Replace
Troca uma string por outra dentro de um texto.. Sintaxe:

"<string>".replace('string que quero mudar', 'nova string')

ou

variavel_do_tipo_string.replace('string que quero mudar', 'nova string')

Exemplos:
```python
a = 'Uma frase bem maneira'
a.replace('bem', 'nada')
```

## Testando suas strings

### Começa com (startswith) ou Termina com (endswith)
Testa se um texto começa/termina com um elemento (é um teste lógico). Sintaxe:

<string>.startswith('primeiras letras')
ou
<string>.endswith('últimas letras')

Exemplos:
```python
a = 'Uma frase bem maneira'
a.startswith('U')

a.startswith('Uma')

a.startswith('bem')

a.endswith('a')

a.endswith('bem maneira')

a.endswith('Uma')
```

