# Atividade 1: Refatorando Localizadores Frágeis
**Enunciado:** No material, vimos que a escolha do localizador determina se o seu teste vai quebrar facilmente quando o layout da página mudar. Imagine que você pegou um teste legado para revisar e encontrou a seguinte linha de código: `await page.locator('.container .form-group:nth-child(3) button').click()`;

**Sua Tarefa:**
1. Explique, com suas palavras, por que o uso de seletores CSS estruturais (como `nth-child` ou classes genéricas) é considerado frágil.
2. Qual é a estratégia de localização mais robusta recomendada pelo material para automação?
3. Reescreva essa linha de código utilizando a melhor prática recomendada, assumindo que você possa pedir para o desenvolvedor adicionar o atributo `data-test="btn-enviar"` no botão.

---

## Por que usar seletores estruturais é ruim?
Nas boas práticas do Playwright, não se é recomendado o uso de seletores estruturais do CSS para os testes automatizados, isso porquê os elementos da página podem ser reorganizados ou a hierarquia mudar futuramente; designers podem alterar as classes; novas divisões (div) podem ser adicionadas; etc.. 

Nesta linha de código, se descreve onde o botão está na estrutura do HTML, e não o que ele é. Dependendo da hierarquia atual; o `nth-child` podendo passar para outro elemento caso o `.form-gourp` ganhar mais um elemento; e as classes genéricas, `.container`, que servem para a estilização:
```typescript
await page.locator('.container .form-group:nth-child(3) button').click();
```

## Qual a estratégia de localização mais robusta?
Se o teste depender da estrutura do DOM, ele poderá quebrar. Por isso é recomendado os usos dos localizadores (locators) para esta tarefa, pois mesmo que a hierarquia dos elementos do HTML ou o CSS da página mude, não terá que reescrever todo os comandos do teste para se adaptar a mudança, pois com os localizadores se é localizado igual ao olhar de um usuário: por seu papel e texto visível, ou até ID.
Um teste:

A recomendação do Playwright é usar os localizadores voltados ao usuário:
- `getByText()` por texto visível: bom para links e rótulos (mas quebra se o texto for traduzido);
- `getByRole()` por papel semântico, pois segue o HTML;
- `getByTestId()` por data-test para automoção robusta.

Mas a prática mais robusta é localizar o elemento por um atributo dedicado a testes (como `data-test` ou `data-testid`), que é estável e independente de estilo, posição ou texto.

## Reescrição de código
Com o atributo data-test="btn-enviar" no botão no HTML, a funcionalidade tem um ID próprio para usar em testes:
```typescript
await page.locator('[data-test="btn-enviar"]').click();
```
O Playwright usa data-testid por padrão no getByTestId, então dá para configurar o atributo no playwright.config.ts:
```typescript
// playwright.config.ts
import { defineConfig } from '@playwright/test';

export default defineConfig({
  use: {
    testIdAttribute: 'data-test',
  },
});
```
E no teste, usar o `getByTestId`:
```typescript
await page.getByTestId('btn-enviar').click();
```

---

<div align="center">
  23/10/2026
</div>
