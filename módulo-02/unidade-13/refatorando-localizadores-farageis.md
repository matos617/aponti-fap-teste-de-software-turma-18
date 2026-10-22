# Atividade 1: Refatorando Localizadores Frágeis
**Enunciado:** No material, vimos que a escolha do localizador determina se o seu teste vai quebrar facilmente quando o layout da página mudar. Imagine que você pegou um teste legado para revisar e encontrou a seguinte linha de código: await page.locator('.container .form-group:nth-child(3) button').click();

**Sua Tarefa:**
1. Explique, com suas palavras, por que o uso de seletores CSS estruturais (como `nth-child` ou classes genéricas) é considerado frágil.
2. Qual é a estratégia de localização mais robusta recomendada pelo material para automação?
3. Reescreva essa linha de código utilizando a melhor prática recomendada, assumindo que você possa pedir para o desenvolvedor adicionar o atributo data-test="btn-enviar" no botão.

---

  Nas boas práticas do Playwright, não se é recomendado o uso de seletores CSS para os testes automatizados, isso porquê os elementos da página podem ser reorganizados ou a hierarquia mudar futuramente; designers podem alterar as classes; novas divisões (div) podem ser adicionadas; etc.. Se o teste depender da estrutura do DOM, ele poderá quebrar. Por isso é recomendado os usos dos localizadores (locators) para esta tarefa, pois mesmo que a hierarquia dos elementos do HTML ou o CSS da página mude, não terá que reescrever todo os comandos do teste para se adaptar a mudança, pois com os localizadores se é localizado igual ao olhar de um usuário: por seu papel e texto visível, ou até ID.

```typescript
await page.locator('.container .form-group:nth-child(3) button').click();
```

