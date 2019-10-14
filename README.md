# Guia do desenvolvedor Python

Olá! Este é um guia de boas práticas para desenvolvedores Python. O objetivo deste material é ilustrar, de forma clara e didática, como um bom código Python deve ser escrito.

## Nomes significativos

Como programadores, nossa criatividade para nomear coisas está, frequentemente, sendo chamada à tona. No dia a dia, precisamos dar nome à diretórios, repositórios, classes, métodos, variáveis, etc. Por isso, conforme [1], devemos nos certificar que estamos fazendo isso bem feito. Além disso, essa boa prática não se trata de uma linguagem de programação ou outra. É válido para qualquer uma!

### Variáveis globais

Assim como em outras linguagens de programação, em Python temos variáveis globais. São aquelas que ficam fora do contexto das funções. Uma variável que está fora do corpo de uma função e só é acessada por outras funções para leitura, é implicitamente global. Além disso, outra forma de se ter uma variável desse tipo é simplesmente declarando-a como global.

As variáveis globais devem ser escritas com todas as letras minúsculas. Ademais, um nome de variável que contenha mais de uma palavra, essas devem ser separadas por um sublinhado.
```python
# Certo
idade = 22
valor_final = 450
# Errado
Idade = 22
valorFinal = 450
```

### Referências

[1] MARTIN, Robert C. **Código Limpo**. Alta Books, 2019.
