# Guia do desenvolvedor Python

Olá! Este é um guia de boas práticas para desenvolvedores Python. O objetivo deste material é ilustrar, de forma clara e didática, como um bom código Python deve ser escrito.

## Nomes significativos

Como programadores, nossa criatividade para nomear coisas está, frequentemente, sendo chamada à tona. No dia a dia, precisamos dar nome à diretórios, repositórios, classes, métodos, variáveis, etc. Por isso, conforme Martin, no livro Código Limpo, devemos nos certificar que estamos fazendo isso bem feito. Além disso, essa boa prática não se trata de uma linguagem de programação ou outra. É válido para qualquer uma!

### Um bom nome de variável

Sempre opte por um nome de variável que exponha (deixe claro) o dado que ela está guardando, ou deverá guardar, em vez de usar um nome curto e sem sentido. Por isso, evite usar nomes de variáveis de uma só letra, como *x* ou *m*. Resumindo, dê nomes que apresentem, de cara, o propósito da existência daquela variável.

Não há, em geral, um limite de tamanho para nomes de variáveis em Python. No entanto, existem algumas convenções que serão apresentadas a seguir.

Em abreviações, devemos colocar todas as letras maiúsculas. Por exemplo: *HTTPServer*.

Em resumo, evite nomes que são muito genéricos, assim como nomes que são muito prolixos.

### Variáveis

Assim como em outras linguagens de programação, em Python temos variáveis globais e locais. As globais são aquelas que ficam fora do contexto das funções. Uma variável que está fora do corpo de uma função e só é acessada por outras funções para leitura, é implicitamente global. Além disso, outra forma de se ter uma variável desse tipo é simplesmente declarando-a como global. Já as variáveis locais são aquelas que são declaradas dentro de uma função e/ou que são declaradas como *self*.

As variáveis devem ser escritas com todas as letras minúsculas. Ademais, um nome de variável que contenha mais de uma palavra, essas devem ser separadas por um sublinhado.
```python
# Certo
idade = 22
valor_final = 450
# Errado
Idade = 22
valorFinal = 450
```

Um nome de variável deve começar com uma letra (a - z) ou um sublinhado. Já os demais caracteres podem ser letras, números ou sublinhados.
```python
# Certo
codigo_item = 45798
_salario = 5000
# Errado
2item = 44
13salario = 5000
```

### Classes

Para as classes, devemos dar nomes seguindo a convenção *CamelCase*. Isto é, as iniciais devem ser maiúsculas, mesmo nos casos em que o nome for composto de mais de uma palavra. Além disso, classes de exceções devem ser finalizadas com o nome "Error".
```python
class Carro:
	# codigo

class SalaDeAula:
	# codigo

class ParserError:
	# codigo
```

### Métodos

Nos casos dos métodos, todas as letras devem ser minúsculas, assim como no caso das variáveis. Além disso, outra convenção semelhante, é que no caso em que o nome de um método seja composto por mais de uma palavra, as mesmas devem ser separadas por um sublinhado. Como adicional, nomes de métodos que não sejam públicos devem iniciar com um sublinhado.
```python
def incluir(this, item):
	# codigo

def somar_debitos(this, compras):
	# codigo
```

## Estrutura do projeto

Quando começamos um projeto, uma das primeiras preocupações que enfrentamos é em relação à organização dos arquivos que estamos criando. Isto é, o repositório do nosso projeto. No caso do Python, existe uma convenção que trata sobre a disposição dos arquivos e diretórios em um projeto.

Além disso, se você está trabalhando em um projeto *open source* e planeja mantê-lo em um repositório online (Github, por exemplo) para que outras pessoas possam utilizar sua produção e/ou contribuir com melhorias, este tópico é muito importante.

A seguir, listamos alguns itens importantes que você deve considerar ter no repositório do seu projeto.

- **LICENSE**: a licença serve para dizer às pessoas o quê elas podem ou não fazer com a sua produção. O arquivo *LICENSE* deve estar no diretório raiz do seu repositório.
- **README**: esse arquivo deve descrever as instruções básicas de uso do seu programa. Assim como no caso da licença, o arquivo *README.md* (feito em Markdown, nesse caso) deve estar no diretório raiz.
- **module**: em alguns casos, esse diretório não é necessário, como naqueles em que você tem apenas um arquivo de código fonte no projeto. No entanto, caso o tenha, esse diretório deve estar, também, na raiz do repositório do projeto. Sendo assim, o código fonte é armazenado dentro do diretório */module*.
- **setup.py**: é muito comum que os projetos feitos em Python tenham um script responsável por fazer o *build* do seu código. Quando houver, deve estar localizado no diretório raiz do repositório.
- **requirements.txt**: um arquivo com os requisitos especificando as dependências que o seu programa precisa para funcionar pode ser bastante útil quando se está utilizando ferramentas como o PIP. Esse arquivo deve estar localizado no diretório raiz.
- **Documentação**: o nome do arquivo é auto explicativo. Os arquivos que dizem respeito à documentação devem ser colocados dentro do diretório */docs*.
- **Testes**: os seus testes devem estar armazenados dentro do diretório */tests.*

Veja abaixo um exemplo de uma disposição de diretórios e arquivos dentro de um repositório bem organizado.
```
docs/conf.py
docs/index.rst
module/__init__.py
module/core.py
tests/core.py
LICENSE
README.md
requirements.txt
setup.py
```

## Referências

- MARTIN, Robert C. **Código Limpo**. Alta Books, 2019.
- Dev Team. **Python Naming Conventions**. 2014. Disponível [neste link](https://visualgit.readthedocs.io/en/latest/pages/naming_convention.html).
- Powell-Morse, Andrew. **Python Best Practices**. 2016. Disponível [neste link](https://airbrake.io/blog/python/python-best-practices).
