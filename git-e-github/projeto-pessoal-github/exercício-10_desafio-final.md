# :rocket: Exercício 10 – Desafio Final

Pesquise outros recursos do Markdown e adicione pelo menos cinco elementos 
diferentes que não foram solicitados nos exercícios anteriores.

## Texto riscado
Este recurso ~~remove ou invalida~~ uma parte do texto:
```
~~Texto~~
```

## Texto destacado
O <mark>texto destacado</mark> é envolvido por `<mark>`:
```
<mark>texto destacado</mark>
```

## HTML dentro do Markdown
<div align="center">
  <h3>Este título está centralizado com HTML.</h3>
</div>

```
<div align="center">
  <h3>Este título está centralizado com HTML.</h3>
</div>
```
> [!IMPORTANT]
> "Centralizar" não é mais aplicável no HTML5, se usa o CSS3 para modificar a aparência, mas no markdown ele funciona.

## Imagens clicáveis
Pode-se usar o HTML5 ou o Markdown para tornar imagens clicáveis:
```
[![Nome pra imagem](url_da_imagem)](url_externo)

ou

<a href="url_do_link_externo"><img src="url_da_imagem" alt=descrição da imagem></a>
```
<div align="center">
  
[![banner](https://thf.bing.com/th/id/R.59c10debb239f9c311619e8374b3fcab?rik=e4dFjyqGob1YdA&riu=http%3a%2f%2fwww.pngall.com%2fwp-content%2fuploads%2f2016%2f05%2fClick-Here-PNG-Images.png&ehk=ggFxsZNlAl5kAmOnXGwvc3MrYRYwHyWu4LKoUSs349A%3d&risl=&pid=ImgRaw&r=0)](https://youtu.be/dQw4w9WgXcQ?si=7R32emRaU-c7PS8n) 

</div>

## Detalhes expansíveis
### `<details>` & `<summary>`
Serve para recolher temporariamente as seções do Markdown, quando clicada ela se expande:
```
<details>

<summary>Título para que os leitores saibam do que se trata</summary>

### Você pode adicionar headers dentro

Pode adicionar texto, imagem e/ou código dentro.

</details>
```
Resultado:

<details>

<summary>Título para que os leitores saibam do que se trata</summary>

### Você pode adicionar headers dentro

Pode adicionar texto, imagem e/ou código dentro.

</details>

## Âncoras
Você pode criar links para seções do próprio documento:
```
[Nome do Título](#nome-do-título)
```

[Ir para o primeiro tópico: ## Texto riscado](#texto-riscado)

## Tabelas avançadas

| Funcionalidade | Estado | Descrição |
|----------------|:-----:|-----------|
| **Login**      | ✅     | Entrar com e‑mail |
| *Registo*      | 🚧     | Suporte a terceiros |
| `Reset`        | ❌     | Redefinir via e‑mail |
| [Perfil](/)    | ⏳     | Gestão de utilizador |

## Escudos personalizados

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-blue?style=flat-square)
![Versão](https://img.shields.io/badge/version-1.0.0-green)
![Contribuições](https://img.shields.io/badge/contributions-welcome-orange)

---

## Extras

### 1. Alertas

Alertas são usados para enfatizar informações críticas, baseadaa no blockquote:

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.

---

## Créditos:
- [Formatações Avançadas](https://github.com/iuricode/readme-template/tree/main/avancado), por GuiMoraesDev.
