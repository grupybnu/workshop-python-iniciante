# venv - Criação de ambientes virtuais

O módulo venv fornece suporte para a criação de "ambientes virtuais" com seus próprios diretórios, opcionalmente isolados dos diretórios do sistema operacional. Cada ambiente virtual tem seu próprio binário Python (que corresponde à versão do binário que foi usada para criar esse ambiente) e pode ter seu próprio conjunto independente de pacotes Python instalados em seus diretórios de sites. Sintaxe:

```
python3 -m venv /path/to/new/virtual/environment
```

## Ativando e desativando um ambiente virtual

Depois que um ambiente virtual é criado, ele pode ser "ativado" usando um script no diretório binário do ambiente virtual. A invocação do script é específica da plataforma (<venv> deve ser substituído pelo caminho do diretório que contém o ambiente virtual):

### Linux e/ou OSX

#### bash/zsh

Ativando:
```shell
$ source <venv>/bin/activate

```

Desativando:
```shell
$ deactivate

```

### Windows

Ativando:
```shell
C:\> <venv>\Scripts\activate.bat

```

Desativando:
```shell
$ deactivate.bat

```