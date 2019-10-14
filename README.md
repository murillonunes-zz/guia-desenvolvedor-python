# Guia do desenvolvedor Python

Olá! Este é um guia de boas práticas para desenvolvedores Python. O objetivo deste material é ilustrar, de forma clara e didática, como um bom código Python deve ser escrito.

## Nomes significativos

Como programadores, nossa criatividade para nomear coisas está, frequentemente, sendo chamada à tona. No dia a dia, precisamos dar nome à diretórios, repositórios, classes, métodos, variáveis, etc. Por isso, conforme [1], devemos nos certificar que estamos fazendo isso bem feito. Além disso, essa boa prática não se trata de uma linguagem de programação ou outra. É válido para qualquer uma!

### Um bom nome de variável

Sempre opte por um nome de variável que exponha (deixe claro) o dado que ela está guardando, ou deverá guardar, em vez de usar um nome curto e sem sentido. Por isso, evite usar nomes de variáveis de uma só letra, como *x* ou *m*. Resumindo, dê nomes que apresentem, de cara, o propósito da existência daquela variável.

Não há, em geral, um limite de tamanho para nomes de variáveis em Python. No entanto, existem algumas convenções que serão apresentadas a seguir.

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

Para as classes, devemos dar nomes seguindo a convenção *CamelCase*. Isto é, as iniciais devem ser maiúsculas, mesmo nos casos em que o nome for composto de mais de uma palavra.

### Métodos

Nos casos dos métodos, todas as letras devem ser minúsculas, assim como no caso das variáveis. Além disso, outra convenção semelhante, é que no caso em que o nome de um método seja composto por mais de uma palavra, as mesmas devem ser separadas por um sublinhado. Como adicional, nomes de métodos que não sejam públicos devem iniciar com um sublinhado.
```python
def incluir(this, item):
	# codigo

def somar_debitos(this, compras):
	# codigo
```

## Referências

[1] MARTIN, Robert C. **Código Limpo**. Alta Books, 2019.
