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
