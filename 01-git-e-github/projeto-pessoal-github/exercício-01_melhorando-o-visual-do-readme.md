# Melhorando o visual do README
Uso da linguagem do Markdown para um melhor visual e a sintaxe do seu repositório no GitHub.

## :pencil2: Títulos e Subtítulos
Hierarquia/Sintaxe: # > ## > ### > #### > ##### > ######
```
# H1 - Título Principal
## H2 - Título da Seção  
### H3 - Título da Subseção
#### H4
##### H5
###### H6
```
Demonstração:
# Título 1 
## SubTítulo 1.1
### Tópico 1.1.1
### Tópico 1.1.2

---

## :abc: Ênfase
Elemento | Sintaxe | Resultado
:--------|:-------:|----------:
Negrito  | `**Texto em negrito** ou __Texto em negrito__`| **Texto em negrito**
Itálico  | `*Texto em itálico* ou _Texto em itálico_`  | *Texto em itálico*
Negrito e Itálico | `***Texto em negrito e itálico*** ou **_Texto em negrito e itálico_**` | ***Texto em negrito e itálico***

---

## :spiral_notepad: Listas enumeradas e com marcadores
### Listas enumeradas (número + ponto)
```
1. Primeiro
2. Segundo
3. Terceiro
4. Quarto
```
Resultado:
1. Primeiro
2. Segundo
3. Terceiro
4. Quarto

### Listas não ordenadas (ó só usar o hífen [-])
- Texto
- Texto 2
- Texto 3

#### itens da lista
Para aninhar itens de linha em uma lista ordenada, recue os itens quatro espaços.
```
1. Primeiro
2. Segundo
3. Terceiro
  1. Indentado intém
  2. Indentado intém
4. Quarto

ou

1. Primeiro
2. Segundo
3. Terceiro
    - Indentado intém
    - Indentado intém
4. Quarto

```
Resultado:
1. Primeiro
2. Segundo
3. Terceiro
    1. Indentado intém
    2. Indentado intém
4. Quarto


1. Primeiro
2. Segundo
3. Terceiro
    - Indentado intém
    - Indentado intém
4. Quarto

---

## :heavy_minus_sign: Linhas horizontais
Há três formas de fazer as linhas de separação:
```
3 Hífens:
---
3 Asteriscos
***
3 Underscore
___
```
Todos dão o mesmo resultado:

### Hífens:
---
### Asteriscos
***
### Underscore
___

---

## :computer: Blocos de código
Pra imitanr o _bash_ se usa ``` (três crases) ou ~~~ (três tils).
~~~
```
Olá Mundo!
```
~~~
Resultado:
```
Olá Mundo!
```
Para ativar a sintaxe de determinado código, se coloca o nome da linguagem ao lado depois dos primeiros tils ou crases:
~~~
```python
print("Olá Mundo!") ```
~~~
Resultado:
```python
print("Olá Mundo!")
```

Para apenas uma linha de código/um código, se usa `` na palavra/código.

Código inline | Resultado
--------------|-----------
``` `código` ```  | `código`

---

## :grinning: Emojis
Para usar um emoji no Markdown, coloque `nome_do_emoji` entre dois pontos (:):

| :bowtie: `:bowtie:` | :smile: `:smile:` | :laughing: `:laughing:` |

Será nescessário buscar o nome de qual emoji irá querer usar, ou simplesmente ir nos emojis do teclado e adicionar.
- [Lista de todos os emojis do GitHub](https://jzeferino.github.io/AllGithubEmojis/)
- [Lista completa da API GitHub Emoji](https://api.github.com/emojis)

---

## :straight_ruler: Tabelas

