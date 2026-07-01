# Melhorando o visual do README
Uso da linguagem do Markdown para um melhor visual e a sintaxe do seu repositório no GitHub.

## Títulos e Subtítulos
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

## Ênfase
Elemento | Sintaxe | Resultado
:--------|:-------:|----------:
Negrito  | `**Texto em negrito** ou __Texto em negrito__`| **Texto em negrito**
Itálico  | `*Texto em itálico* ou _Texto em itálico_`  | *Texto em itálico*
Negrito e Itálico | `***Texto em negrito e itálico*** ou **_Texto em negrito e itálico_**` | ***Texto em negrito e itálico***

---

## Listas enumeradas e com marcadores
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

#### itens da lista
Para aninhar itens de linha em uma lista ordenada, recue os itens quatro espaços.
```
1. Primeiro
2. Segundo
3. Terceiro
  1. Indentado intém
  2. Indentado intém
4. Quarto
```
Resultado:
1. Primeiro
2. Segundo
3. Terceiro
    1. Indentado intém
    2. Indentado intém
4. Quarto

---

## Linhas horizontais
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

## Blocos de código
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

## Emojis

---

## Tabelas
