# Loops (Repetições)
A execução repetitiva do mesmo bloco de código repetidamente é chamada de iteração. No Python temos 2 estruturas de repetição que são elas:

- [for](#for)
- [while](#while)

Nessas duas estruturas de repetição podemos utilizar as seguintes declarações:
- break: Interromper a execução do loop
- continue: Pular a execução do loop

Exemplos:
```python
a = [1,2,3,4,5]

i = 0
while a[i] < 4:
    print(a[i])
    i += 1
    break

for i in a:
    print(i)
    break

i = 0
while a[i] < 4:
    if i == 2:
        continue
    print(a[i])
    i += 1

for i in a:
    if i == 1:
        continue
    print(i)
```

No caso do for podemos usar a condição "else" caso a lista não tenha valores vai pode executar alguma ação.

Exemplos:
```python
for i in []:
    print(i)
else:
    print('nenhum valor encontrado!')
```

## for
São tradicionalmente usados quando você tem um bloco de código que você deseja repetir um número fixo de vezes.

Exemplos:
```python
a = [1,2,3,4,5]

for i in a:
    print(i)
```

## while
Ao contrário de um loop for, o loop while não será executado n vezes, mas até que uma condição definida não seja mais atendida. Se a condição for inicialmente falsa, o corpo do loop não será executado.

Exemplos:
```python
a = [1,2,3,4,5]

i = 0
while a[i] < 4:
    print(a[i])
    i += 1
```
