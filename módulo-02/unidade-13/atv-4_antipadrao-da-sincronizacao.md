# Atividade 4: O Antipadrão da Sincronização
**Enunciado:** Durante a execução de um teste no servidor de CI/CD, um elemento da tela demorou um pouco mais para carregar e o teste falhou. Para "corrigir" o problema rapidamente, um colega adicionou a seguinte linha no código: `await page.waitForTimeout(5000)`;

**Sua Tarefa:**
1. Explique por que o uso do `waitForTimeout()` é classificado como um antipadrão (uma prática ruim que deve ser evitada). O que acontece com o teste quando a página é rápida e quando ela é muito lenta?
2. O Playwright possui um mecanismo de Auto-wait. O que esse mecanismo faz antes de executar uma ação como um click()?
3. Como você reescreveria essa espera de forma inteligente, utilizando um `expect().toBeVisible()` para aguardar o elemento `.tabela-resultados` aparecer na tela?

---

## 1. Por que `waitForTimeout()` é considerado um antipadrão?
O `waitForTimeout()` faz o teste esperar um tempo fixo, independentemente de a página já estar carregada ou não.

Isso causa dois problemas:

- Quando a página é rápida, o teste continua esperando os 5 segundos, mesmo que o elemento já tenha carregado. Isso aumenta o tempo de execução desnecessariamente;
- Quando a página é muito lenta e o elemento demorar mais de 5 segundos para aparecer, o teste falhará mesmo que ele eventualmente carregue.

Além de que o Playwright já tem um mecanismo automático.

## 2. O que é o Auto-wait do Playwright?
O Auto-wait é um mecanismo automático do Playwright que verifica se um elemento já está pronto antes de executar uma ação, como um `click()`.

Antes de clicar, ele verifica se o elemento:
- Está visível na tela;
- Está estável, sem mudanças de posição;
- Está habilitado para receber interações;
- Não está bloqueado por outro elemento.

Se o elemento ainda não estiver pronto, o Playwright aguarda automaticamente, dentro do limite de tempo configurado.

## 3. Como reescrever a espera utilizando `expect().toBeVisible()`?
Ao invês de utilizar uma espera fixa de 5 segundos, dá pra utilizar uma condição que aguarda até que o elemento esteja visível.

```typescript
import { test, expect } from '@playwright/test';

test('Verificar se a tabela de resultados aparece', async ({ page }) => {
    await page.goto('baseUrl');

    await expect(page.locator('.tabela-resultados')).toBeVisible();
});
```

- `page.locator('.tabela-resultados')`: localiza o elemento pelo seletor CSS.
- `expect()`: inicia uma verificação.
- `toBeVisible()`: verifica se o elemento está visível na tela.

O Playwright verifica a condição repetidamente até que ela seja atendida ou o tempo limite seja atingido. Assim, o teste não come o tempo com tempos fixos, e sim se atende as condições para continuar.
