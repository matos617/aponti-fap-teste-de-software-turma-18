# Atividade 4: O Antipadrão da Sincronização
**Enunciado:** Durante a execução de um teste no servidor de CI/CD, um elemento da tela demorou um pouco mais para carregar e o teste falhou. Para "corrigir" o problema rapidamente, um colega adicionou a seguinte linha no código: `await page.waitForTimeout(5000)`;

**Sua Tarefa:**
1. Explique por que o uso do `waitForTimeout()` é classificado como um antipadrão (uma prática ruim que deve ser evitada). O que acontece com o teste quando a página é rápida e quando ela é muito lenta?
2. O Playwright possui um mecanismo de Auto-wait. O que esse mecanismo faz antes de executar uma ação como um click()?
3. Como você reescreveria essa espera de forma inteligente, utilizando um expect().toBeVisible() para aguardar o elemento .tabela-resultados aparecer na tela?

---
