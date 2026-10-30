# Atividade 3: Asserts - Escolhendo o Matcher Correto
**Enunciado:** Validar resultados é a alma do teste automatizado. O material faz uma distinção importante entre `toHaveText()` e `toContainText()`. Imagine o seguinte cenário: após cadastrar um usuário, o sistema exibe uma mensagem de sucesso na tela que inclui um número de protocolo gerado dinamicamente: "Cadastro realizado com sucesso! Protocolo: 987654".

**Sua Tarefa:**
1. Qual dos dois asserts (`toHaveText` ou `toContainText`) você deve utilizar para validar essa mensagem, sabendo que o número do protocolo muda a cada teste?
2. Justifique sua escolha com base nas características de cada comando mostradas no material.
3. Escreva como ficaria a linha de código do assert, assumindo que a mensagem aparece em um elemento com a classe .toast-message

---
## `toHaveText` x `toContainText`
`toHaveText` (exato) compara o texto completo do elemento com o valor esperado, já o `toContainText` (parte) verifica apenas se o texto informado está presente no conteúdo do elemento. Como o número do protocolo muda a cada execução, o texto nunca será o mesmo, logo, usar o `toHaveText` não funcionaria neste cenário, pois ele exige match exato, mas o teste só precisa validar a parte fixa da mensagem.
Para lidar com informações dinâmicas, o `toContainText` é a melhor escolha.

```typescript
await expect(page.locator('.toast-message')).toContainText('Cadastro realizado com sucesso!');
```
