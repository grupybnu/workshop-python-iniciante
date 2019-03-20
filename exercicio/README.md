# Exercício

Nesse exercício vamos praticar alguns conceitos sobre o ambiente e a linguagem Python.
Para a prática, vamos usar a _SWAPI_ (`https://swapi.co/`) ou _The Star Wars API_.
A ideia é que vamos fazer requisições para essa API e mostrar alguns resultados na tela.
Sem mais, vamos as atividades.

## 1. Criar um diretório para o projeto (se quiser, pode iniciar um repositório git)

## 2. Crie e inicie um ambiente virtual

Aqui você pode iniciar um ambiente virtual que desejar: `venv`, `pipenv`, `conda`.

## 3. Instale a biblioteca `requests` no ambiente virtual

Para instalar um pacote você usa `pip install <pacote>`

## 4. Faça uma requisição de teste

* Crie um arquivo `teste.py`
* Importe a biblioteca `requests`
* Importe a biblioteca `json` (padrão do python)
* Faça uma requisição para `https://swapi.co/api/people/1/` usando `requests.get`
* Converta o conteúdo _JSON_ da requisição em um `dict` utilizando a biblioteca `json`
* Imprima `Hello, <name>!` no _console_
* Execute `python teste.py`
* Deve imprimir `Hello, Luke Skywalker!`

_obs_: ao invés de usar a biblioteca padrão do python para obter o _JSON_, poderíamos
usar o método `r.json()` disponível na requisição da biblioteca `requests`.

## 5. Crie uma aplicação que procura os dados de um personagem

* Crie um arquivo `main.py` e outro `star_wars.py`
* O arquivo `main.py` só deve ter a lógica de entrada e exibição de dados
* O arquivo `star_wars.py` vai ter a lógica de comunicação com o _SWAPI_
* Receba um parâmetro `nome` no `main.py` e imprima as seguintes informações:
`name`, `height`, `birth_year` e a _quantidade de filmes que ele aparece_.
```
# exemplo

python main.py --nome "Luke Skywalker"
* Nome: Luke Skywalker
* Altura: 172cm
* Ano de nascimento: 19BBY
* Quantidade de filmes: 5

python main.py --nome "Meu nome"
* Personagem "Meu nome" não encontrado

```

_dicas_:
* Uma requisição para `https://swapi.co/api/people/` retorna todos os personagens
    * O resultado é paginado de 10 em 10 personagens
    * Portanto, se não encontrar na página atual, tem que seguir para a página no atributo `next`
* A comparação dos nomes deve ser _case insensitive_, ou seja, `luke skywalker == LUKE SKYWALKER`

## 6. Faça _matching_ parcial dos nomes

Na mesma aplicação, se encontrar um personagem com um nome exatamente igual,
mostre as informações dele (feito na parte anterior).
Entretanto, permita uma pesquisa parcial do nome.
Por exemplo, `python main.py --nome "Skywalker"` deve imprimir as informações de
_Luke Skywalker_ e _Anakin Skywalker_.

_obs_: você pode optar por uma das opções:
* Opção 1:
    * `python main.py --nome "Skywalker"`
    * Se encontrou um nome exatamente igual, exibe essas informações
    * Se não, exibe todos os nomes que contém a pesquisa
* Opção 2:
    * `python main.py --nome "%Skywalker%"`
    * Note os caractéres _%_ no nome
    * Quando esses caractéres estiverem no parâmetro de entrada, a pesquisa deve ser parcial
    * Caso contrário, a pesquisa é exata

## 7. Se não encontrar pelo termo pesquisado, de sugestões

Quando recebemos entradas no formato `python main.py --nome "Skywalker"`, pode ser que
ocorra um erro de digitação, por exemplo `python main.py --nome "Skywaler"`.
Nesse caso, seria interessante mostrar para o usuário uma mensagem do tipo
_Nenhum personagem "Skywaler" encontrado, mas encontrei: "Luke Skywalker", "Anakin Skywalker"_.

Para resolver esse problema, podemos usar a biblioteca [`fuzzywuzzy`](https://github.com/seatgeek/fuzzywuzzy).
Basta instalar a biblioteca e comparar as strings com 
`fuzz.partial_ratio('skywaler', 'Luke Skywalker')`. 
Essa função retorna um "grau de confiança" entre 0 e 100.
Portanto, podemos assumir que, se houve comparação perfeita ou parcial (partes 5 e 6), você pode sugerir os nomes que tenham um grau de confiança maior que 75.
```
# exemplo
python main.py --nome "skywaler"
Nenhum personagem "Skywaler" encontrado, mas encontrei: "Luke Skywalker", "Anakin Skywalker"

# nesse exemplo, não encontrou nenhum personagem com nome "skywaler"
# mas ao calcular fuzz.partial_ratio('skywaler', 'Luke Skywalker')
# temos um grau de confiança de 88, logo pode ser que o usuário quis dizer "Luke Skywalker"
# ao invés de "skywaler"
# o mesmo acontece com fuzz.partial_ratio('skywaler', 'Anakin Skywalker')
```

## 8. A imaginação é o limite

Que tal tentar adicionar novos comandos ao `main.py`?
Pode ser um comando para listar os `n` personagens que mais aparecem em filmes.
Outro ideia é listar os filmes de forma ordenada pela quantidade de personagems que aparecem no filme.
Outras ideias? Vá em frente e tente :D
